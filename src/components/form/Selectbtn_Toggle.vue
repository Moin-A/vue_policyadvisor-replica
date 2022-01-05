<template>
	<div :class="'col-md-' + col">
		<p>Gender</p>

		<div class="row">
			<div class="col pr-0">
				<input
					type="radio"
					checked
					class="d-none"
					:name="inputname_default"
					:id="`label`+this.id+`a`"
				/>
				<label
					class="smok btn w-100 my-2 "
					:for="`label`+this.id+`a`"		
				>{{innertext.first}}</label>
			</div>
			<div class="col pl-0">
				<input
					type="radio"
					:name="inputname_default"
					class="d-none"
					:id="`label`+this.id+`b`"
				/>
				<label
					class="nsmok btn  w-100 my-2"
					:for="`label`+this.id +`b`"		
				>{{innertext.second}}</label>
			</div>
		</div>
	</div>
</template>

<script>
	const uniqueId = require('lodash.uniqueid');

	export default {

		name: "BTNTGL",
		created() {
		this.id = uniqueId()
		
		},
		mounted() {


		},
		computed: {
			inputname_default(){
				if (this.inputname=="") return "inputname-"+this.id;
				return this.inputname;
			
			}
		},
		props: {
			inputname: {
				type:String,
				default: ""
				
			},
			col: {
				type: Number,
				default: 5,
				required: true
			},
			innertext: {
				type: Object,
				dafault: { first: "male", second: "female" }
			}



		},
		data: function () {
			return {

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
