<template>

	<div :class="'col-md-' + col">
		<div>
			<p>{{titletext}}</p>
			<div class="row">
				<div class="col-11 pr-0">
					<select class="w-100 py-2 cursor-pointer form-control">
						<option v-for="Option  in Options" :key="Option"  >{{Option}} </option>	
					</select>
				</div>
			</div>
		</div>
	</div>
	<!-- <div class="col-7">
				<p>Coverage</p>
				<div class="row m-0">
					<div class="col pl-0">
						<input
							type="range"
							class="form-range w-100"
							id="customRange1"
						/>
						<div class="d-flex justify-content-between">
							<p><small>$25,000</small></p>
							<p><small>$5 million</small></p>
						</div>
					</div>
				</div>
			</div> -->

</template>

<script>


	export default {

		name: "BTNDROPDWN",

		props: {
			col: {
				type: Number,
				default: 5
			},
			titletext: {
				type: String,
				default: "TERM"
			},

			Options: {
				type: Array,

				default: () => (
					["5 Years","15 Years","20 Years","25 Years","30 Years"]

				)
			}
		}



	}
</script>

<style scoped>
h4,
p {
	color: black;
}

p {
	text-align: left;
}

span {
	text-align: left;
}
lable {
	margin: 0 10px;
}

.smok,
male {
	border-radius: 3px 0px 0px 3px !important;
}

.nsmok,
fmale {
	border-radius: 0px 3px 3px 0px !important;
}
label {
	border-color: #d5d4d6;
}
label:hover {
	color: #17b3e4;
	border: 1px solid #17b3e4;
}
select,
option {
	color: #17b3e4;
}
input[type='radio']:checked + label {
	font-weight: bold;
	background-color: #17b3e4;
	color: #fff;
}
input[type='range']::-webkit-slider-thumb {
	appearance: none;
	width: 23px;
	height: 24px;
	border: 0;
	background-image: url('~@/assets/logo.png');
	cursor: pointer;
}
input[type='radio']:checked + label {
	font-weight: bold;
	background-color: #17b3e4;
	color: #fff;
}
</style>
