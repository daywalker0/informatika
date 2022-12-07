<script setup>
</script>

<template>
	<div class="opponentTwo">
		<div class="opponentTwo__inner">
			<span>Соперник №2</span>
		</div>
	</div>
</template>

<style lang="scss" scoped>
.opponentTwo {
	border-top-left-radius: 10px;
	border-bottom-left-radius: 10px;
	position: absolute;
	z-index: 50;
	right: 0;
	top: 47%;
	height: 100px;
	width: 755px;
	background-color: #fff;
	&::after {
		content: '';
		position: absolute;
		left: 0;
		bottom: 0;
	}
	&__inner {
		padding: 30px;
		span {
			font-size: 35px;
			font-weight: 700;
			margin-left: 50px;
		}
	}
}

</style>