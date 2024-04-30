<script>
  import { Link } from "svelte-routing";
  import { handleAnchorClick } from "../../js/handleAnchorClick";

  import AndiPicture from "../../assets/andi-picture.png";

  import SkillCard from "../components/SkillCard.svelte";
</script>

<!-- My Personal Portfolio -->
<div class="mt-56">
  <h1
    class="relative z-10 mb-8 text-center text-5xl font-bold tracking-wide sm:text-6xl lg:w-3/5 lg:text-left lg:text-8xl"
  >
    MY PERSONAL PORTFOLIO
  </h1>
  <div
    class="flex flex-col justify-center gap-4 text-2xl sm:flex-row lg:justify-start"
  >
    <button class="z-10 rounded-lg bg-white text-main-orange"
      ><Link to="/gallery" class="block h-full w-full px-10 py-4">Explore</Link
      ></button
    >
    <a
      href="#contact"
      class="z-10 px-10 py-4 text-center sm:text-left"
      on:click={handleAnchorClick}>How To Hire Me</a
    >
  </div>
</div>

<!-- Who Am I -->
<div class="mt-96 lg:mt-80">
  <h2 class="mb-12 text-center text-4xl font-semibold lg:-mb-16">
    - WHO AM I -
  </h2>
  <div class="grid grid-cols-1 items-center gap-x-12 lg:grid-cols-2">
    <div
      class="flex flex-col gap-8 text-justify text-xl sm:text-2xl md:text-3xl"
    >
      <p>
        My name is Muhammad Vieri Farhandi. I am a designer from Indonesia,
        Jakarta, and I'm still in college at UPH University (Universitas Pelita
        Harapan) in Karawaci. If you're looking for website design, posters, or
        photo editing, I'm the guy to help.
      </p>
    </div>
    <div class="relative -mt-16 lg:mt-0">
      <img
        src={AndiPicture}
        alt="Author Profile"
        class="relative z-10 rounded-3xl"
      />
      <div class="absolute bottom-0 h-3/4 w-full rounded-xl bg-[#acb8e8]"></div>
    </div>
  </div>
</div>

<!-- Want To Hire Me -->
<div class="mt-48">
  <h2 class="mb-24 text-center text-4xl font-semibold sm:mb-36">
    - MY SKILLS -
  </h2>

  <div class="grid grid-cols-1 gap-x-8 gap-y-24 md:grid-cols-2 lg:grid-cols-3">
    <SkillCard
      skill="Photoshop"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Adobe_Photoshop_CC_icon.svg/2101px-Adobe_Photoshop_CC_icon.svg.png"
      alt="Photoshop logo"
    />
    <SkillCard
      skill="Illustrator"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Adobe_Illustrator_CC_icon.svg/2101px-Adobe_Illustrator_CC_icon.svg.png"
      alt="Illustrator logo"
    />
    <SkillCard
      skill="Figma"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Figma-logo.svg/1667px-Figma-logo.svg.png"
      alt="Figma Logo"
    />
  </div>
</div>
