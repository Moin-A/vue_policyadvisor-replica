<template>
	<div class="form bg-white">
		<h4>Get instant Quotes</h4>
		<div class="row">

			<Selectbtn
				:col="5"
				:innertext="innerText"
				inputname="gender"
			/>

			<Selectbtn
				:col="5"
				:innertext="innerText"
				inputname="smoking"
			/>

		</div>
		<!-- //---Date of Birth-------// -->

		<div class="row mt-3">
			<InputBTNTEXT
				:col="5"
				titletext="Date of Birth"
				placeholder="DD/MM/YYYY"
			/>
			<InputBTNTEXT
				:col="5"
				placeholder="A1A 1A1"
				titletext="Postal Code"
			/>

		</div>
		<!-- //---TERM-------// -->
		<div class="row mt-3">
			<BTNDROPDWN
				:col="5"
				titletext="TERM"
				:Options='["5 Years","15 Years","20 Years","25 Years","30 Years"]'
			/>
			<BTNRANGE
				:col="7"
				titletext="TERM"
				:range="{'min':'$25,000','max':'$5 million'}"	
			/>
		</div>
	</div>
	<div class="form-submit p-4">
		<div class="row">
			<div class="col monthly-prem">
				<span class="font-weight-bold">Monthly Premium</span>
				<div>---</div>
			</div>
			<div class="col m-auto">
				<SubmitButton>
					COMPARE QUOTES
				</SubmitButton>
			</div>
		</div>
	</div>
</template>

<script>
	import Selectbtn from './form/Selectbtn_Toggle.vue'
	import InputBTNTEXT from './form/Inputbtn-Text.vue'
	import BTNDROPDWN from './form/Selectbtn_Dropdown.vue'
	import BTNRANGE from './form/Selectbtn_range.vue'
	import SubmitButton from "./Buttons/SubmitButton.vue"

	export default {
		name: 'Widget',
		data: function () {
			return {
				innerText: {
					first: "male",
					second: "female"

				},
			}
		},

		components: {
			Selectbtn,
			InputBTNTEXT,
			BTNDROPDWN,
			BTNRANGE,
			SubmitButton

		},
		createperson: function (firstName, lastName) {
			this.firstName = firstName
			this.lastName = lastName
		}

	}
</script>

<style scoped>
.form {
	border-top: 8px solid #17b3e4;
	padding: 20px;
	box-shadow: 0px 3px 10px rgb(0 0 0 / 10%);
	background: #ffffff;
	-webkit-box-shadow: 0px 3px 10px rgb(0 0 0 / 10%);
	box-shadow: 0px 3px 10px rgb(0 0 0 / 10%);
	border-top: 8px solid #17b3e4;
	margin: auto;
	font-family: lato, sans-serif;
}

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
.form-range {
	display: flex;
	flex-direction: column;
}

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

.monthly-prem div {
	font-size: 34px;
	font-weight: 600;
	line-height: 41px;
	min-height: 50px;
	color: #17b3e4;
}
</style>
