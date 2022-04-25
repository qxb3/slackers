<script>
	import 'bulma/css/bulma.css'

	import Navbar from './components/Navbar.svelte'

	import Home from './routes/home/index.svelte'
	import Rules from './routes/Rules.svelte'
	import Members from './routes/Members.svelte'
	import NotFound from './routes/NotFound.svelte'

	import router from 'page'
	let page

	router('/', () => (page = Home))
	router('/rules', () => (page = Rules))
	router('/members', () => (page = Members))
	router('/*', () => (page = NotFound))

	router.start()
</script>

<svelte:head>
	<link href="https://fonts.googleapis.com/css?family=Didact Gothic" rel='stylesheet'>
	<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.0/css/all.min.css" rel="stylesheet">
	<style>
		* {
			box-sizing: border-box;
		}

		html, body {
			font-family: "Didact Gothic";
			padding: 0;
		}
	</style>
</svelte:head>

<Navbar />

<main>
	<svelte:component this={page} />
</main>
