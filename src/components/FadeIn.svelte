<script>
	// TODO: Fix this thing

	import IntersectionObserver from 'svelte-intersection-observer'

	export let direction

	let element = null
	let isIntersecting = false
</script>

<IntersectionObserver once {element} bind:intersecting={isIntersecting}>
	<div
		bind:this={element}
		class:fade-in={isIntersecting && (!direction || direction === "none")}
		class:fade-in-top={isIntersecting && direction === "top"}
		class:fade-in-bottom={isIntersecting && direction === "bottom"}
		class:fade-in-left={isIntersecting && direction === "left"}
		class:fade-in-right={isIntersecting && direction === "right"}
		class:hidden={isIntersecting === false}
		class:visible={isIntersecting}
	>
		<slot></slot>
	</div>
</IntersectionObserver>

<style>
	.hidden {
		visibility: hidden;
	}

	.visible {
		visibility: visible;
	}

	.fade-in {
		-webkit-animation: fade-in 1.3s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
		animation: fade-in 1.3s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	}

	@-webkit-keyframes fade-in {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}

	@keyframes fade-in {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}

	.fade-in-top {
		-webkit-animation: fade-in-top 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
		animation: fade-in-top 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	}

	@-webkit-keyframes fade-in-top {
		0% {
			-webkit-transform: translateY(-50px);
			transform: translateY(-50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateY(0);
			transform: translateY(0);
			opacity: 1;
		}
	}

	@keyframes fade-in-top {
		0% {
			-webkit-transform: translateY(-50px);
			transform: translateY(-50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateY(0);
			transform: translateY(0);
			opacity: 1;
		}
	}

	.fade-in-bottom {
		-webkit-animation: fade-in-bottom 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
		animation: fade-in-bottom 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	}

	@-webkit-keyframes fade-in-bottom {
		0% {
			-webkit-transform: translateY(50px);
			transform: translateY(50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateY(0);
			transform: translateY(0);
			opacity: 1;
		}
	}

	@keyframes fade-in-bottom {
		0% {
			-webkit-transform: translateY(50px);
			transform: translateY(50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateY(0);
			transform: translateY(0);
			opacity: 1;
		}
	}

	.fade-in-left {
		-webkit-animation: fade-in-left 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
		animation: fade-in-left 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	}

	@-webkit-keyframes fade-in-left {
		0% {
			-webkit-transform: translateX(-50px);
			transform: translateX(-50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateX(0);
			transform: translateX(0);
			opacity: 1;
		}
	}

	@keyframes fade-in-left {
		0% {
			-webkit-transform: translateX(-50px);
			transform: translateX(-50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateX(0);
			transform: translateX(0);
			opacity: 1;
		}
	}

	.fade-in-right {
		-webkit-animation: fade-in-right 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
		animation: fade-in-right 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	}

	@-webkit-keyframes fade-in-right {
		0% {
			-webkit-transform: translateX(50px);
			transform: translateX(50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateX(0);
			transform: translateX(0);
			opacity: 1;
		}
	}

	@keyframes fade-in-right {
		0% {
			-webkit-transform: translateX(50px);
			transform: translateX(50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateX(0);
			transform: translateX(0);
			opacity: 1;
		}
	}
</style>
