<script>
	const previews = [
		{
			img: '/images/activities/party.png',
			description: 'We have an active members all over the map that is ready to party and grind with you!'
		},
		{
			img: '/images/activities/celebrate.png',
			description: 'Want some cool screenshots? join now xd'
		},
		{
			img: '/images/activities/giveaways.png',
			description: 'We sometimes do a  public or guild giveaways The prizes are golds, items, scrolls and more!'
		}
	]
</script>

<div class="previews">
	{#each previews as preview}
		<div class="card">
			<div class="card-image">
				<figure class="image is-4by2">
					<img src={preview.img} alt="">
				</figure>
			</div>

			<div class="content">
				{preview.description}
			</div>
		</div>
	{/each}
</div>

<style>
	.previews {
		display: flex;
		justify-content: space-around;
	}

	.card {
		margin: 16px;
		flex-basis: 100%;
	}

	.content {
		padding: 16px;
	}

	@media (max-width: 600px) {
		.previews {
			flex-direction: column;
		}
	}
</style>
