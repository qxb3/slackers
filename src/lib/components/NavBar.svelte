<script>
  import { AppBar, modalStore } from '@skeletonlabs/skeleton'
  import { links } from '$lib/vars.js'

  function openMenu() {
    modalStore.trigger({
      type: 'component',
      component: 'navLinks',
      position: 'items-start'
    })
  }
</script>

<AppBar regionRowMain="container">
  <svelte:fragment slot="lead">
    <a class="btn flex items-center justify-center" href="/">
      <img src="/logo.png" alt="Logo" width="40" height="auto" />
      <h1 class="h1 text-2xl text-primary-400">Slackers</h1>
    </a>
  </svelte:fragment>

  <svelte:fragment slot="trail">
    <button on:click={openMenu} class="md:hidden btn py-5 px-4 rounded-md border-surface-900 border-2">
      <i class="fa fa-bars fa-lg"></i>
    </button>

    <div class="hidden md:block">
      <ul class="flex items-center space-x-5">
        {#each links as link}
          <li>
            <a href={link.href}>
              <i class={link.icon}></i>
              {link.text}
            </a>
          </li>
        {/each}
      </ul>
    </div>
  </svelte:fragment>
</AppBar>
