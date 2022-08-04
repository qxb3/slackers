<script>
	import membersJson from '../../public/assets/members.json'

	const { leaders } = membersJson
	const { commanders } = membersJson
	const { knights } = membersJson.members
	const { rangers } = membersJson.members
	const { mages } = membersJson.members
	const { shamans } = membersJson.members
</script>

<div class="container">
	<div class="members">
		<div class="group">
			<h1 class="title is-size-4 mb-3">Leaders</h1>
			<ol>
				{#each leaders as leader}
					<li>{leader}</li>
				{/each}
			</ol>
		</div>

		<div class="group">
			<h1 class="title is-size-4 mb-3">Commanders</h1>
			<ol>
				{#each commanders as commander}
					<li>{commander}</li>
				{/each}
			</ol>
		</div>

		<div class="group">
			<h1 class="title is-size-4 mb-3">Knights</h1>
			<ol>
				{#each knights as knight}
					<li>{knight}</li>
				{/each}
			</ol>
		</div>

		<div class="group">
			<h1 class="title is-size-4 mb-3">Rangers</h1>
			<ol>
				{#each rangers as ranger}
					<li>{ranger}</li>
				{/each}
			</ol>
		</div>

		<div class="group">
			<h1 class="title is-size-4 mb-3">Mages</h1>
			<ol>
				{#each mages as mage}
					<li>{mage}</li>
				{/each}
			</ol>
		</div>

		<div class="group">
			<h1 class="title is-size-4 mb-3">Shamans</h1>
			<ol>
				{#each shamans as shaman}
					<li>{shaman}</li>
				{/each}
			</ol>
		</div>
	</div>
	</div>

<style>
	.members {
		padding: 16px;
	}

	.group {
		margin-bottom: 24px;
	}

	ol {
		list-style-position: inside;
	}
</style>
