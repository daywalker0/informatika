<script setup>
import { reactive } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

// import required modules
import { Mousewheel } from "swiper";
const modules = [Mousewheel]

const hexData = reactive ([
	{
		name: "Стадион",
		date: '30 сентября',
		time: '19:00'
	},
	{
		name: "Стадион",
		date: '16 июля',
		time: '19:00'
	},
	{
		name: "Стадион",
		date: '26 июня',
		time: '19:00'
	},
	{
		name: "Стадион",
		date: '17 июня',
		time: '19:00'
	},
	{
		name: "Стадион",
		date: '30 июня',
		time: '19:00'
	},

])
</script>

<template>
	<swiper
		:direction="'vertical'"
		:slidesPerView="5"
		:centeredSlides="true"
		:initialSlide="2"
		:spaceBetween="0"
		:mousewheel="true"
		:modules="modules"
		class="mySwiper"
	>
		<swiper-slide v-for="(hex, index) in hexData" :key="hex">
			<div class="hexagon">
				<div class="fill">
					<div class="hexagon__content">
						<div class="hexagon__name">{{ hex.name }}</div>
						<div class="hexagon__date">{{ hex.date }}</div>
						<div class="hexagon__time">{{ hex.time }}</div>
						<button class="hexagon__btn">Купить билет</button>
					</div>
				</div>
			</div>
		</swiper-slide>
	</swiper>
</template>

<style lang="scss">
.swiper {
	transform: rotate(58deg);
	height: 1300px;
	margin: -200px -140px 0 0;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
	transition: 1s;
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide-active {
	margin-top: 30px;
	.hexagon {
		transform: scale(2.25) rotate(32deg);
		transition: .6s;
	}
}

.swiper-slide-prev {
	margin-bottom: 30px;
	.hexagon {
		transform: scale(1.5) rotate(32deg);
	}
}
.swiper-slide-next {
	margin-top: 60px;
	.hexagon {
		transform: scale(1.5) rotate(32deg);
	}
}

.hexagon,
.hexagon::before,
.hexagon::after {
  background-color: #fff;
}

.fill,
.fill::before,
.fill::after {
  background-color: #fff;
}

.hexagon::before,
.hexagon::after {
  transform: translateX(-50%) scaleY(0.7) rotate(45deg);
}

.hexagon {
  position: relative;
  margin: 3rem;
  width: 7.1rem;
  height: 4rem;
  font-size: 2rem;
	transform: rotate(32deg);
	&__content {
		position: absolute;
		z-index: 10;
		transform: rotate(-90deg);
		font-size: 10px;
		font-weight: 400;
		bottom:-20px;
		right: 20px;
	}
	&__date {
		font-size: 20px;
		font-weight: 500;
		margin: 10px 0;
	}
	&__btn {
		margin-top: 10px;
		background: none;
		border: 1px solid black;
		@include br(5px);
		font-size: 10px;
		white-space: nowrap;
		padding: 5px;
		cursor: pointer;
		transition: .3s;
		&:hover {
			transition: .3s;
			background: #08238a;
			border-color: #08238a;
			color: #fff;
		}
	}
}

.hexagon::before,
.hexagon::after {
  content: "";
  position: absolute;
  width: 5.4rem;
  height: 5.4rem;
}

.hexagon::before {
  top: -2.7rem;
  left: 50%;
	@include br(10px)
}

.hexagon::after {
  bottom: -2.7rem;
  left: 50%;
	@include br(10px)
}

.fill {
  position: absolute;
  left: 50%;
  top: 50%;
  width: 7rem;
  height: 3.5rem;
  z-index: 1;
  transform: translate(-50%, -50%);
}

.fill::before,
.fill::after {
  content: "";
  position: absolute;
  width: 5rem;
  height: 5rem;
  transform: scaleY(0.7) rotate(45deg);
}

.fill::before {
  top: -2.5rem;
  left: 1rem;
}

.fill::after {
  bottom: -2.5rem;
  left: 1rem;
}






</style>
