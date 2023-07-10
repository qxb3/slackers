<script>
  import members from './members.json'
</script>

<svelte:head>
  <title>Slackers Members List</title>
</svelte:head>

<div class="container p-4">
  <div class="text-center max-w-xs mx-auto">
    <h1 class="mt-4 text-3xl text-primary-400">
      <i class="fas fa-users-crown"></i>
      Members List
      <i class="fas fa-users-crown"></i>
    </h1>

    <div class="mt-2 h-[0.1px] bg-primary-400 w-7/12 mx-auto"></div>
  </div>

  <div class="overflow-x-auto mt-12">
    <table class="table table-auto">
      <thead class="table-header-group">
        <tr class="table-row">
          <th class="table-cell">
            <i class="fas fa-swords"></i>
            Role
          </th>

          <th class="table-cell">
            <i class="fas fa-user"></i>
            Name
          </th>

          <th class="table-cell">
            <i class="fas fa-sitemap"></i>
            Rank
          </th>

          <th class="table-cell">
            <i class="fas fa-question"></i>
            Status
          </th>
        </tr>
      </thead>

      <tbody class="table-row-group">
        {#each members as { role, name, rank, status }}
          <tr class="table-row">
            {#if role === 'knight'}
              <td class="table-cell">
                <i class="fas fa-helmet-battle"></i>
                Knight
              </td>
            {:else if role === 'ranger'}
              <td class="table-cell">
                <i class="fas fa-bow-arrow"></i>
                Ranger
              </td>
            {:else if role === 'mage'}
              <td class="table-cell">
                <i class="fas fa-staff"></i>
                Mage
              </td>
            {:else if role === 'shaman'}
              <td class="table-cell">
                <i class="fas fa-wand-magic"></i>
                Shaman
              </td>
            {/if}

            <td class="table-cell">{name}</td>

            {#if rank === 'leader'}
              <td class="table-cell">
                <i class="fas fa-crown"></i>
                Leader
              </td>
            {:else if rank === 'vice_leader'}
              <td class="table-cell">
                <i class="fas fa-shield-alt"></i>
                Vice Leader
              </td>
            {:else if rank === 'member'}
              <td class="table-cell">
                <i class="fas fa-bed"></i>
                Member
              </td>
            {/if}

            <td class="table-cell">
              {#if status === 'active'}
                <div class="inline-block w-4 h-4 rounded-full bg-success-400"></div>
                Active
              {:else if status === 'inactive'}
                <div class="inline-block w-4 h-4 rounded-full bg-error-400"></div>
                Inactive
              {/if}
            </td>
          </tr>
        {/each}
      </tbody>
    </table>
  </div>
</div>
