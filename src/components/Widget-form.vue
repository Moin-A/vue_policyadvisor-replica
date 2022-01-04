<template>
	<div class="form bg-white">
		<h4>Get instant Quotes</h4>
		<div class="row">

			<Selectbtn
				:col="5"
				v-bind:innertext="innerText"
			/>

			<Selectbtn
				:col="5"
				v-bind:innertext="innerText"
			/>

		</div>
		<!-- //---Date of Birth-------// -->
		<div class="row mt-3">
			<div class="col-5">
				<div>
					<p>Date of Birth</p>
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
			<div class="col-7">
				<p>Postal Code</p>
				<div class="row m-0">
					<div class="col pl-0">
						<input
							type="text"
							id="post_code"
							name="post_code"
							placeholder="A1A 1A1"
							class="form-control form__input"
						/>
					</div>
				</div>
			</div>
		</div>
		<!-- //---TERM-------// -->
		<div class="row mt-3">
			<div class="col-5">
				<div>
					<p>Term</p>
					<div class="row">
						<div class="col-11 pr-0">
							<select class="w-100 py-2 cursor-pointer form-control">
								<option value="0">10 years</option>
								<option value="1">15 Years</option>
								<option
									selected
									value="2"
								>20 Years</option>
								<option value="3">25 Years</option>
								<option value="4">30 Years</option>
								<option value="5">35 Years</option>
								<option value="6">40 years</option>
								<option value="7">To Age 65</option>
							</select>
						</div>
					</div>
				</div>
			</div>
			<div class="col-7">
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
			</div>
		</div>
	</div>
	<div class="form-submit p-4">
		<div class="row">
			<div class="col monthly-prem">
				<span class="font-weight-bold">Monthly Premium</span>
				<div>---</div>
			</div>
			<div class="col m-auto">
				<button
					type="submit"
					class="btn btn-lg text-white"
				>
					Compare Quotes
				</button>
			</div>
		</div>
	</div>
</template>

<script>
	import Selectbtn from './form/Selectbtn_Toggle.vue'

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
