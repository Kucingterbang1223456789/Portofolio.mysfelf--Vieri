<script>
  import { register } from "swiper/element/bundle";

  import skecthMoutain from "../../assets/sketch-gunung.jpg";
  import skecthBanana from "../../assets/sketch-pisang.jpg";
  import banner from "../../assets/youtube_banner_2-01.png";
  import calendar from "../../assets/january1_copy_yes-01.png";
  import halo from "../../assets/kartu_nama_2-1.png";

  register();

  let currentIndex = 0;

  const onSlideChange = (e) => {
    const [swiper, progress] = e.detail;
    currentIndex = swiper.snapIndex;
  };

  const artworkDescriptions = [
    {
      title: "Mountain Sketch",
      description:
        "This art project explores the intricacies of mountain landscapes through meticulous sketching. Each line and shade conveys the essence of towering peaks, inviting viewers to appreciate the artistry of nature. Through this detailed depiction, the project aims to inspire wonder and reverence for Earth's majestic heights.",
    },
    {
      title: "Calendar",
      description:
        "This project transcends utility, transforming a digital calendar into a canvas of artistic expression. Each element, meticulously crafted with vector graphics, embodies elegance and creativity. Vibrant colors and sleek lines merge functionality with aesthetic appeal, offering users a daily dose of visual inspiration.",
    },
    {
      title: "Banana Sketch",
      description:
        "This art project delves into the aesthetics of a banana, capturing its organic contours and unique texture through intricate linework and shading. By elevating this simple subject into a detailed artwork, the sketch invites viewers to appreciate the beauty of everyday objects in a new light.",
    },
    {
      title: "YouTube Banner",
      description:
        "This art project reimagines YouTube banners through vector artistry. Every detail, from vibrant colors to precise shapes, is meticulously crafted to convey creativity and professionalism. Each element harmonizes to form a visually compelling and cohesive design, elevating the banner into a captivating piece of digital art.",
    },
    {
      title: "Card Design",
      description:
        "This art project showcases the intersection of design and artistry through a vector-based card creation. Clean lines, sophisticated colors, and intricate patterns define this piece, embodying creativity and precision. Each element is thoughtfully composed, transforming the card into a unique and visually striking work of art.",
    },
  ];
</script>

<!-- My Artwork -->
<div class="mt-36 sm:mt-56">
  <h1
    class="relative z-10 mb-8 text-center text-5xl font-bold tracking-wide sm:text-6xl lg:w-3/5 lg:text-left lg:text-8xl"
  >
    MY ARTWORK
  </h1>
</div>

<!-- Artwork Description -->
<div class="mt-24 flex items-center justify-center lg:mt-36">
  <div class="z-10 w-11/12 max-w-2xl text-justify leading-normal">
    <h2 class="text-center text-4xl font-bold lg:text-6xl">
      {artworkDescriptions[currentIndex].title}
    </h2>
    <p class="mt-12 text-base sm:text-xl">
      {artworkDescriptions[currentIndex].description}
    </p>
  </div>
</div>

<!-- Artwork Slideshow -->
<swiper-container
  class="mySwiper mt-16"
  effect="coverflow"
  grab-cursor={true}
  centered-slides={true}
  slides-per-view="auto"
  coverflow-effect-rotate={50}
  coverflow-effect-stretch={0}
  coverflow-effect-depth={100}
  coverflow-effect-modifier={1}
  coverflow-effect-slide-shadows={true}
  pagination={false}
  on:swiperslidechange={onSlideChange}
>
  <swiper-slide>
    <img src={skecthMoutain} alt="Gunung" />
  </swiper-slide>
  <swiper-slide>
    <img src={calendar} alt="Calendar" />
  </swiper-slide>
  <swiper-slide>
    <img src={skecthBanana} alt="Banana" />
  </swiper-slide>
  <swiper-slide>
    <img src={banner} alt="Youtube Banner" />
  </swiper-slide>
  <swiper-slide>
    <img src={halo} alt="Card Name" />
  </swiper-slide>
</swiper-container>

<style>
  swiper-container {
    width: 100%;
  }

  swiper-slide {
    background-position: center;
    background-size: cover;
    width: 75%;
    height: 75%;
  }

  swiper-slide img {
    display: block;
    width: 100%;
  }
</style>
