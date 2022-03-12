<div class='activities'>
	<div class='item'>
		<img src='/images/activities/party.png' alt='activity' />
		<div class='item-description'>
			<p>We have an active members all over the map that is ready to party and grind with you!</p>
		</div>
	</div>
	<div class='item'>
		<img src='/images/activities/celebrate.png' alt='activity' />
		<div class='item-description'>
			<p>Want some cool screenshots? Join now xd</p>
		</div>
	</div>
</div>

<style>
	.activities {
		display: flex;
		justify-content: space-evenly;
	}

	.item {
		box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
		margin: 16px;
		max-width: 362px;
		flex-basis: 100%;
		flex-grow: 0;
	}

	.activities .item img {
		width: 100%;
		height: 204px;
		object-fit: cover;
	}

	.item-description {
		padding: 12px;
	}

	@media (max-width: 600px) {
		.activities {
			flex-direction: column
		}
	}
</style>
