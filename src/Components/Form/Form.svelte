<script>
	import Clarifai from 'clarifai'
	const apiKey = __myapp.env.API_KEY
	const app = new Clarifai.App({
<<<<<<< HEAD
		apiKey: apiKey,
=======
		apiKey: '',
>>>>>>> 89df43e5fa0f1c5ce0e566f3ce9644afc185ac56
		apiEndpoint: 'https://api.clarifai.com'
	})

	let imgUrl
	const handleSubmit = () => {
		app.models
      .predict(
        // HEADS UP! Sometimes the Clarifai Models can be down or not working as they are constantly getting updated.
        // A good way to check if the model you are using is up, is to check them on the clarifai website. For example,
        // for the Face Detect Mode: https://www.clarifai.com/models/face-detection
        // If that isn't working, then that means you will have to wait until their servers are back up. Another solution
        // is to use a different version of their model that works like: `c0c0ac362b03416da06ab3fa36fb58e3`
        // so you would change from:
        // .predict(Clarifai.FACE_DETECT_MODEL, this.state.input)
        // to:
        // .predict('c0c0ac362b03416da06ab3fa36fb58e3', this.state.input)
        Clarifai.FACE_DETECT_MODEL,
        imgUrl)
      .then(response => {
        console.log('hi', response)
          })
	}
</script>
<style>

</style>
<div>
	<form  on:submit|preventDefault="{handleSubmit}">
		<input 
			type="text"
			bind:value="{imgUrl}"
		/>
		<input 
			type="submit"
		/>
	</form>
</div>
