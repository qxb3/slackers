<script>
  import { page } from '$app/stores'

  const notFound = [
    'You have ventured into the unknown. Page not found!',
    'A wild 404 appears! It uses \'Missing Page\'. It\'s super effective!',
    '404 Error: Dungeon entrance collapsed. No way forward!',
    'You\'ve encountered a mystical 404. Try another path!',
    'You search high and low, but this 404 page eludes you.',
    '404 Error: The dragon ate this page. It was too spicy!',
    'Sorry, hero. The treasure you seek is on another page. 404!'
  ]
</script>

<div class="container h-96 p-4">
  <div class="flex flex-col items-center justify-center h-full text-center max-w-xs mx-auto">
    <h1 class="h1 text-primary-400 mb-2">{$page.status}</h1>
    {#if $page.status === 404}
      <h3 class="h3">{notFound[Math.floor(Math.random() * 6)]}</h3>
    {:else}
      <h3 class="h3">{$page.error.message}</h3>
    {/if}
  </div>
</div>
