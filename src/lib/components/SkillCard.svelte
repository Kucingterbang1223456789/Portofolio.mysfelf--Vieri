<script>
  export let skill = "";
  export let src = "";
  export let alt = "";
</script>

<div
  class="text-main-orange relative flex h-96 w-full items-center justify-center rounded-3xl bg-white text-4xl font-semibold"
>
  <div
    class="bg-main-orange absolute -top-12 flex w-24 items-center justify-center rounded-xl p-4"
  >
    <img {src} {alt} class="h-16" />
  </div>
  <p>{skill}</p>
</div>
