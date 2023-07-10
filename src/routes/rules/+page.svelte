<script>
  import { Accordion, AccordionItem } from '@skeletonlabs/skeleton'

  let rules = [
    {
      title: 'English Language Only',
      full: 'This is a Nordic lead guild, and we communicate exclusively in English in guild-chats.',
      icon: 'fa-language'
    },
    {
      title: 'Respect and Consequences',
      full: 'We expect respectful behavior from all players, and any inappropriate actions will have consequences. Zero tolerance against racism and sexism.',
      icon: 'fa-ban'
    },
    {
      title: 'Membership Voting Process',
      full: 'A person can become a guild member after successfully passing the voting process, which requires 18 hours or a majority vote.',
      icon: 'fa-vote-yea'
    },
    {
      title: 'Guild Information on Discord',
      full: 'Every guild member must regularly read the information published on Discord when they are able to do so.',
      icon: 'fa-info-circle'
    },
    {
      title: 'Supportive Community',
      full: 'The guild aims to provide advice, assistance, and share experiences with those who need it.',
      icon: 'fa-hands-helping'
    },
    {
      title: 'Responsible Expression of Opinions',
      full: 'All players have the right to voice their opinions, as long as they are not irresponsible personal attacks made in the heat of the moment.',
      icon: 'fa-comments'
    },
    {
      title: 'Maintaining a Good Reputation',
      full: 'Both inside and outside the guild, members should behave in a manner that does not tarnish the guild\'s reputation. This includes in-game channels like "trade" and "local" games with other players.',
      icon: 'fa-thumbs-up'
    },
    {
      title: 'Dispute Resolution',
      full: 'Any problems arising from disputes between players should be reported to the guild leaders.',
      icon: 'fa-exclamation-circle'
    },
    {
      title: 'KOS List and Player Hunt',
      full: 'If a player is added to the KOS (kill on sight) list by the leaders, all members are required to add this player to their friendlist, report their locations, and actively hunt them until they have paid the consequences.',
      icon: 'fa-crosshairs'
    },
    {
      title: 'Guild Colors',
      full: 'Members should use the guild colors for their characters: black head and brown body. Alternate options include cyan head and brown body, brown head and black body, and dark red head and black body.',
      icon: 'fa-palette'
    },
    {
      title: 'Leaving and Rejoining',
      full: 'Leaving Slackers without a valid reason or leaving to join another guild will result in a permanent ban from rejoining Slackers.',
      icon: 'fa-door-closed'
    }
  ]

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
