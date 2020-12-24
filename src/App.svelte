<script>
	import Navigation from './Components/Navigation/Navigation.svelte'
	import Form from './Components/Form/Form.svelte'
	import OutputBox from './Components/OutputBox/OutputBox.svelte'
</script>
<Navigation />
<main>
	<Form />
	<OutputBox />
</main>

<style>
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>