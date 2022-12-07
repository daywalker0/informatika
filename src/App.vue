<script setup>
import TheHeader from './components/TheHeader.vue';
import Slider from './components/Slider.vue'
import OpponentOne from './components/OpponentsBlocks/OpponentOne.vue'
import OpponentTwo from './components/OpponentsBlocks/OpponentTwo.vue'
</script>

<template>
	<div class="wrapper">
		<TheHeader />
		<OpponentOne />
		<Slider />
		<OpponentTwo />
	</div>
</template>

<style lang="scss">
.wrapper {
	min-height: 100vh;
	overflow: hidden;
	background: rgb(0,212,255);
	background: radial-gradient(circle, rgba(0,212,255,1) 0%, rgba(4,120,194,1) 0%, rgba(9,9,121,1) 0%, rgba(7,55,151,1) 0%, rgba(8,35,138,1) 12%, rgba(9,9,121,1) 28%, rgba(9,9,121,1) 30%, rgba(2,0,36,1) 66%);
	position: relative;
	&::after {
		@include pseudo;
		@include br(100%);
		border: 1px solid #fff;
		width: 60%;
		top: -2%;
		height: 95%;
		left: 21%;
	}
	&::before {
		@include pseudo;
		@include br(100%);
		border: 1px solid #fff;
		width: 35%;
		top: 16%;
		height: 58%;
		left: 34%;
	}
}
</style>