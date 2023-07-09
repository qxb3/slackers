<script>
  const showcases = [
    {
      image: 'party.png',
      text: 'We have an active members all over the map that is ready to party and grind with you!'
    },
    {
      image: 'celebrate.png',
      text: 'Want some cool screenshots? join now xd'
    },
    {
      image: 'giveaways.png',
      text: 'We sometimes do a public or guild giveaways The prizes are golds, items, scrolls and more!'
    }
  ]
</script>

<svelte:head>
  <title>Join Slackers</title>
</svelte:head>

<div class="container p-4">
  <div class="text-center">
    <h1 class="h1 text-5xl md:text-7xl mt-6 text-primary-400 underline underline-offset-4 decoration-2">Slackers</h1>
    <h2 class="h2 mt-1">The guild that just wants to slack.</h2>

    <a href="https://discord.gg/xKwBfkFkPw" class="btn btn-lg variant-filled-primary mt-3">
      <span>Join Now</span>
      <span>
        <i class="fas fa-arrow-right"></i>
      </span>
    </a>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 mt-5">
    {#each showcases as showcase}
      <div class="card bg-surface-300 text-center p-3 m-2 h-full">
        <img src="/screenshots/{showcase.image}" alt="Showcase" />
        <p class="mt-3">{showcase.text}</p>
      </div>
    {/each}
  </div>
</div>
