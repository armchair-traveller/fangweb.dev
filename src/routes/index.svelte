<style>
  a {
    display: contents;
    @apply font-bold;
    @apply hover:underline;
  }
  a img {
    object-fit: cover;
    border-radius: 16px;
    margin: 1rem 0;
  }
</style>

<svelte:head>
  <title>Fang's Website · Now With 110% More JAM</title>
  <link
    rel="icon"
    href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='12 0 100 100'><text y='.9em' font-size='90'>🦁</text></svg>" />
</svelte:head>

<main class="p-7 md:px-28 max-w-4xl space-y-4">
  <h1 class="text-lg font-semibold">Hi there!</h1>
  <p>
    I'm
    <a rel="external" href="https://github.com/armchair-traveller">Fang</a>, a
    front end developer passionate in the JAM stack and serverless.
  </p>
  <p>
    I like to poke, prod, and experiment with the particulars of my tech stack,
    so you'd likely find a long list if I went over it all. My GitHub profile
    goes into detail about what tech I've used, and projects I've worked on.
  </p>
  <p>We still have space, so here's a little taste:</p>
</main>

<section class="bg-black ">
  <div class="px-7 py-1 md:px-28">
    <a rel="external" href="https://bearcoffee.netlify.app/"><img
        src="/images/bear_coffee.webp"
        alt="Bear Coffee preview" /></a>
    <a rel="external" href="https://toucanrecipes.netlify.app/"><img
        src="/images/toucan_recipes.webp"
        alt="Toucan Recipes preview" /></a>
  </div>
</section>
