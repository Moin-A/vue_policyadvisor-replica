
<template>
	<div :class="'col-md-' + col">
		<div>
			<p>{{titletext}}</p>
			<div class="row">
				<div class="col-11 pr-0">
					<input
						id="branding_date_of_birth"
						name="branding_date_of_birth"
						pattern="[0-9]*"
						inputmode="numeric"
						type="text"
						placeholder="DD/MM/YYYY"
						blur="function () { [native code] }"
						class="form-control form__input form__input--error"
					/>
				</div>
			</div>
		</div>
	</div>
	

</template>

<script>
	

	export default {
		name: "InputBTNTEXT",
 
		props: {

			col: {
				type: Number,
				default: 5,
				required: true
			},
			titletext: {
				type: String,
				default: "",
			
			}




		},








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
    