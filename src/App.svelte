<script>
	import Navigation from './Components/Navigation/Navigation.svelte'
	import Form from './Components/Form/Form.svelte'
</script>
<Navigation />
<main>
	<Form />
</main>

<style>
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>