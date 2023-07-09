<script>
  import { modalStore } from '@skeletonlabs/skeleton'

  const links = [
    { href: '/', text: 'Home', icon: 'fas fa-home' },
    { href: '/members', text: 'Members', icon: 'fas fa-user-group' },
    { href: '/rules', text: 'Rules', icon: 'fas fa-scroll' },
  ]

  function closeMenu() {
    modalStore.close()
  }
</script>

<div class="card w-[97%] !bg-surface-900 p-4">
  <div class="flex justify-between">
    <ul class="text-lg space-y-1 w-full">
      {#each links as link}
        <li>
          <a class="block py-2 px-1" href={link.href}>
            <i class={link.icon}></i>
            {link.text}
          </a>
        </li>
      {/each}
    </ul>

    <div>
      <button on:click={closeMenu} class="btn btn-sm">
        <i class="fas fa-x"></i>
      </button>
    </div>
  </div>

  <div class="w-[97%] h-[0.1px] bg-white mx-auto my-4"></div>

  <div>
    <a href="/" class="btn variant-filled-primary">
      <span>Join Now</span>
      <span>
        <i class="fas fa-arrow-right"></i>
      </span>
    </a>
  </div>
</div>
