<script>
	import Header from './components/Header.svelte'
	import Content from './components/Content.svelte'
	import Footer from './components/Footer.svelte'
</script>

<svelte:head>
	<link href='https://fonts.googleapis.com/css?family=Didact Gothic' rel='stylesheet'>
	<style>
		*, *:before, *:after {
			box-sizing: inherit;
		}

		html, body {
			box-sizing: border-box;
			font-family: 'Didact Gothic';
			padding: 0;
		}
	</style>
</svelte:head>

<Header />
<Content />
<Footer />
