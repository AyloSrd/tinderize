<script>
	export let width
	export let height
	export let faceBoxData

	const boxDetails = faceBoxData.region_info.bounding_box

	const top = Number(boxDetails.top_row)*height
	const left = Number(boxDetails.left_col)*width
	const boxWidth = (Number(boxDetails.right_col) - Number(boxDetails.left_col))*width
	const boxHeight = (Number(boxDetails.bottom_row) - Number(boxDetails.top_row))*height	
	
	const style = `position: absolute; top: ${top}px; left: ${left}px; height: ${boxHeight}px; width: ${boxWidth}px; z-index:5000;`
</script>
<style>
	.faceBox {
		box-shadow: 0 0 0 3px #149df2 inset;
		background-color: #149df2;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		cursor: pointer;
	}
</style>
<div 
	class="faceBox"
	{ style }
></div>