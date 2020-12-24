<script>

	export let width
	export let height
	export let faceBoxData

	
	let top = Number(faceBoxData.region_info.bounding_box.top_row)*height
	let left = Number(faceBoxData.region_info.bounding_box.left_col)*width
	let boxWidth = (Number(faceBoxData.region_info.bounding_box.right_col) - Number(faceBoxData.region_info.bounding_box.left_col))*width
	let boxHeight = (Number(faceBoxData.region_info.bounding_box.bottom_row) - Number(faceBoxData.region_info.bounding_box.top_row))*height
	
	console.log(top)
	
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
	style="position: absolute; top: {top}px; left: {left}px; height: {boxHeight}px; width: {boxWidth}px; z-index:5000;"
></div>