<script>
	import GuildPreview from './components/GuildPreview.svelte'
	//import Backstory from './components/Backstory.svelte'
	import JoinInstruction from './components/JoinInstruction.svelte'
</script>

<div class="container">
	<div class="guild-description">
		<h1 class="title">Slackers</h1>
		<h1 class="subtitle">Slackers (SLS) is a non-toxic guild that has over 100+ members</h1>
	</div>

	<GuildPreview />
	<!--<Backstory />-->
	<JoinInstruction />
</div>

<style>
	.container {
		text-align: center;
		margin-top: 32px;
	}

	.guild-description {
		max-width: 80%;
		margin: auto;
		margin-bottom: 16px;
	}
</style>
