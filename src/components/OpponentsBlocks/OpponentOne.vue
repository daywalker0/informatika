<script setup>
</script>

<template>
	<div class="opponentOne">
		<div class="opponentOne__inner">
			<span>Соперник №1</span>
		</div>
	</div>
</template>

<style lang="scss" scoped>
.opponentOne {
	border-top-right-radius: 10px;
	border-bottom-right-radius: 10px;
	position: absolute;
	z-index: 50;
	top: 32%;
	height: 105px;
	width: 765px;
	background-color: #fff;
	&::after {
		content: '';
		position: absolute;
		right: 0;
		bottom: 0;
	}
	&__inner {
		padding: 30px;
		text-align: end;
		span {
			font-size: 35px;
			font-weight: 700;
			margin-right: 50px;
		}
	}
}

@media (max-width: 1440px) {
	.opponentOne {
		width: 550px;
	}
}
</style>
