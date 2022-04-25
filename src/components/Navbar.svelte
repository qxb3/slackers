<script>
	let isActive = false
	const changeState = () => (isActive = !isActive)
	const close = () => (isActive = false)
</script>

<nav class="navbar is-dark has-shadow is-spaced">
	<div class="navbar-brand">
		<a on:click={close} href="/" class="navbar-item">
			<img src="/images/logo.png" alt="" />
			<h1>Slackers</h1>
		</a>

		<div on:click={changeState} class="navbar-burger" class:is-active={isActive}>
			<span></span>
			<span></span>
			<span></span>
		</div>
	</div>

	<div class="navbar-menu" class:is-active={isActive}>
		<div class="navbar-end">
			<a on:click={close} href="/rules" class="icon-text navbar-item">
				<span class="icon">
					<i class="fa fa-scroll"></i>
				</span>
				<span>Rules</span>
			</a>

			<a on:click={close} href="/members" class="icon-text navbar-item">
				<span class="icon">
					<i class="fa fa-user-group"></i>
				</span>
				<span>Members</span>
			</a>
		</div>
	</div>
</nav>

<style>
	a {
		text-decoration: none;
	}

	.navbar-menu {
		background-color: hsl(0, 0%, 21%);
	}

	.navbar-menu a {
		color: white;
	}
</style>
