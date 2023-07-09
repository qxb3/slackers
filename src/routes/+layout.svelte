<script>
  import {
    AppShell,
    Modal
  } from '@skeletonlabs/skeleton'

  import NavBar from '$lib/components/NavBar.svelte'
  import NavLinks from '$lib/components/modals/NavLinks.svelte'

  import '@skeletonlabs/skeleton/styles/skeleton.css'
  import '../theme.css'
  import '../app.css'

  const modalComponentRegistry = {
    navLinks: {
      ref: NavLinks
    }
  }
</script>

<Modal
  components={modalComponentRegistry}
  duration="0"
  regionBackdrop="bg-surface-backdrop-token backdrop-blur-sm"
/>

<AppShell>
  <svelte:fragment slot="header">
    <NavBar />
  </svelte:fragment>

  <slot />

  <svelte:fragment slot="footer">(footer)</svelte:fragment>
</AppShell>
