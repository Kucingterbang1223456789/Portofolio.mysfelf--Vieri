<script>
  import { Router, Link, Route } from "svelte-routing";

  import Background from "./assets/BackgroundMain.svelte";
  import Navbar from "./lib/components/Navbar.svelte";
  import ArtworkPage from "./lib/pages/ArtworkPage.svelte";
  import HomePage from "./lib/pages/HomePage.svelte";
</script>

<main class="bg-gradient-to-b from-[#666] to-[#111] font-poppins text-white">
  <Router>
    <div class="mx-auto w-11/12 max-w-7xl">
      <!-- Navigation Bar -->
      <div class="pt-8">
        <Navbar />
      </div>

      <Background />

      <Route path="/" component={HomePage} />
      <Route path="/gallery" component={ArtworkPage} />
    </div>

    <!-- Contact -->
    <footer id="contact" class="mt-36 bg-main-orange sm:mt-52">
      <div class="mx-auto w-11/12 max-w-7xl py-12">
        <div
          class="flex flex-col items-start justify-between gap-8 sm:flex-row"
        >
          <div>
            <p class="mb-6 text-2xl font-bold">Follow Me</p>
            <div class="flex flex-col gap-3">
              <a
                href="https://api.whatsapp.com/send/?phone=6281280729617&text&type=phone_number&app_absent=0"
                target="_blank">Whatsapp</a
              >
              <a
                href="https://www.instagram.com/vieriandi20?igsh=bThhOWdvNDg1ZGpn"
                target="_blank">Instagram</a
              >
              <a
                href="https://twitter.com/FarhandiVieri?t=P0zzSB5WJUf4LClW-fltoQ&s=33"
                target="_blank">Twitter</a
              >
              <a href="https://line.me/ti/p/farhandi12" target="_blank">Line</a>
            </div>
          </div>

          <div>
            <p class="mb-6 text-2xl font-bold">Pages</p>
            <div class="flex flex-col gap-3">
              <Link to="/">Home</Link>
              <Link to="/gallery">My Gallery</Link>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </Router>
</main>
