<template>
	<header>
		<div class="row justify-content-around">
			<div class="col-4 col-lg-2 my-auto">
				<img
					alt="Vue logo"
					src="../../images/policyadvisor-logo.svg"
				/>
			</div>
			<div class="row">
				<div class="text-right  px-2">
					<p>Need help? Speak to one of our advisors.</p>
					<p>Call 1-888-601-9980</p>
				</div>
				<div class="px-2">
					<img
						alt="Vue logo"
						src="../../assets/profile-logo.png"
					/>
				</div>
			</div>
		</div>
	</header>

</template>


<script>
	export default {
		name: "Header",

	}
</script>

<style scoped>
header {
	background-color: #001e4c;
	padding: 10px 40px;
}
p:last-child {
	font-size: 24px;
}
p {
	font-family: 'Lato';
	font-size: 16px;
	font-weight: 600;
	color: #fff;
	margin-bottom: 6px;
}
</style>