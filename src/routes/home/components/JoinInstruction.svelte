<div class="instruction">
	<p class="title has-text-white is-size-4">How to join?</p>

	<p>Click the <strong>Join now</strong> button to join our official discord server and go to the <strong>#apply-to-slackers</strong> channel</p>
	<button class="join" on:click={() => window.open("https://discord.gg/74uEjq4rZE", "_blank")}>
		<img src="/images/discord.png" alt="" />
		<p>Join now</p>
	</button>
</div>

<style>
	.instruction {
		background-color: #2c2f33;
		color: white;
		padding: 32px;
		text-align: center;
	}

	.join {
		display: flex;
		align-items: center;
		justify-content: space-evenly;
		margin: 24px auto 0 auto;
		padding: 6px;
		background-color: #121212;
		border-width: 0;
		color: white;
		box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
		cursor: pointer;
	}

	strong {
		color: white;
	}

	.join > * {
		margin: 6px;
	}

	.join img {
		width: 28px;
		height: 28px;
	}

	.join:hover {
		background-color: #404040;
	}
</style>
