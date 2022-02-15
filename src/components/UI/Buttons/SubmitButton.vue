<template>
    <button
					type="submit"
					class="btn btn-lg text-white"
				>
                <slot/>
    </button>            
</template>

<script>


export default {
    name:"Button"
}
</script>


<style scoped>
.form-submit {
	background: #e5faff;
}
input[type='range']::-webkit-slider-thumb {
	-webkit-appearance: none; /* Override default look */
	appearance: none;
	width: 25px; /* Set a specific slider handle width */
	height: 25px; /* Slider handle height */
	background: #04aa6d; /* Green background */
	cursor: pointer; /* Cursor on hover */
}

.btn-lg {
	background: #d81671;
	font-weight: 600;
}
</style>
