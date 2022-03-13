<footer>
	<div class='content-container'>
		<h3>How to join?</h3>
		<p>Click the <strong>Join now</strong> button to join our official discord server and go to the <strong>#apply-to-slackers</strong> channel</p>
		<button on:click={() => window.open('https://discord.gg/74uEjq4rZE', '_blank')}>Join now</button>
	</div>
	<div class='links-container'>
		<a href='https://github.com/qxb3/slackers' target='_blank'>
			<img src='https://cdn-icons-png.flaticon.com/512/25/25231.png' alt='repository' />
		</a>
	</div>
</footer>

<style>
	footer {
		background-color: #2c2f33;
		color: white;
	}

	.content-container {
		padding: 32px 32px 12px 32px;
		text-align: center;
	}

	button {
		margin-top: 8px;
		padding: 14px;
		background-color: #121212;
		border-width: 0;
		color: white;
		box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
		transition: 0.6;
	}

	.links-container {
		display: flex;
		justify-content: end;
	}

	img {
		margin: 8px;
		width: 40px;
		height: 40px;
	}
</style>
