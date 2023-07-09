<script>
  import { Accordion, AccordionItem } from '@skeletonlabs/skeleton'
  import { rulesList } from '$lib/vars.js'

  let rules = rulesList

  function select(index) {
    rules = rules.map(v => ({ ...v, selected: false }))

    const rule = rules.find((_, v) => index === v)
    rule.selected = true

    rules[index] = rule
  }
</script>

<svelte:head>
  <title>Slackers Rules</title>
</svelte:head>

<div class="container p-4">
  <div class="text-center max-w-xs mx-auto">
    <h1 class="mt-4 text-3xl text-primary-400">
      <i class="fas fa-scroll fa-sm"></i>
      Rules
      <i class="fas fa-scroll fa-sm"></i>
    </h1>

    <div class="mt-2 h-[0.1px] bg-primary-400 w-2/5 mx-auto"></div>

    <p class="mt-3">Please read keep this rules in mind when joining the guild or even you are already joined the guild.</p>
  </div>

  <div class="mt-9">
    <Accordion
      autocollapse
      spacing="space-y-3"
      regionPanel="border border-t-0 border-surface-200 rounded-tl-none rounded-tr-none"
    >
      {#each rules as rule, i}
        <AccordionItem
          on:click={() => select(i)}
          regionControl={rule.selected ? 'border border-surface-200 text-primary-400' : 'border border-surface-500'}
        >
          <svelte:fragment slot="lead">
            <i class="fas {rule.icon}"></i>
          </svelte:fragment>
          <svelte:fragment slot="summary">{rule.title}</svelte:fragment>
          <svelte:fragment slot="content">{rule.full}</svelte:fragment>
        </AccordionItem>
      {/each}
    </Accordion>
  </div>
</div>
