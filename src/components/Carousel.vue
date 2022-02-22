<template>
	<Carousel :autoplay="4000" :itemsToShow="3" :wrapAround="true" class="mt-10">
		<Slide v-for="(slide, index) in slides" :key="index">
			<div
				class="px-5 py-14 grid justify-center items-center text-white border-white border rounded lg:h-96 h-full transform hover:scale-105 hover:shadow-xl hover:bg-white hover:text-black cursor-pointer lg:w-full w-28"
			>
				<div class="mb-0 text-4xl">
					{{ slide.emo }}
				</div>
				<div class="text-center my-8 px-10">
					{{ slide.summary }}
				</div>
				<div class="flex lg:flex-row flex-col lg:mx-4 mx-0">
					<div><img :src="slide.img" alt="" class="mx-auto" /></div>
					<div class="px-8">
						<div class="text-base font-semibold">{{ slide.name }}</div>
						<div class="text-xs">{{ slide.title }}</div>
					</div>
				</div>
			</div>
		</Slide>

		...
	</Carousel>
</template>

<script>
import { defineComponent } from 'vue';
import { Carousel, Pagination, Slide } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';
import img1 from '../assets/test-img1.svg';
import img2 from '../assets/test-img2.svg';
import img3 from '../assets/test-img3.svg';

export default defineComponent({
	name: 'Autoplay',
	components: {
		Carousel,
		Slide,
		Pagination,
	},
	data() {
		return {
			slides: [
				{
					img: img1,
					emo: ' 🤩 ',
					title: 'Chess grandmaster',
					name: 'Magnus Carlsen',
					summary:
						'“Easy to order, smooth delivery with top-notch quality furnitures. Great experience overall”',
				},
				{
					img: img2,
					emo: ' 😍 ',
					title: 'Social Media Influencer',
					name: 'James Brown',
					summary:
						'“Very intentional, thoughtful and beautiful design. Just the right fit to my office space.”',
				},
				{
					img: img3,
					emo: ' 😄 ',
					title: 'Actress',
					name: 'Emilia Clarke',
					summary: '“My sofa has become my best friend, Thanks to you.”',
				},
				{
					img: img2,
					emo: ' 😍 ',
					title: 'Social Media Influencer',
					name: 'James Brown',
					summary:
						'“Very intentional, thoughtful and beautiful design. Just the right fit to my office space.”',
				},
			],
		};
	},
});
</script>

<style scoped>
.carousel__item {
	min-height: 200px;
	width: 100%;
	background-color: transparent;
	color: var(--vc-clr-white);
	font-size: 20px;
	border-radius: 8px;
	display: flex;
	justify-content: center;
	align-items: center;
}

.carousel__slide {
	padding: 10px;
}

.carousel__prev,
.carousel__next {
	box-sizing: content-box;
	border: 5px solid white;
}
.carousel__slide > .carousel__item {
	transform: scale(1);
	opacity: 0.5;
	transition: 0.5s;
}
.carousel__slide--visible > .carousel__item {
	opacity: 1;
	transform: rotateY(0);
}
.carousel__slide--next > .carousel__item {
	transform: scale(0.9) translate(-10px);
}
.carousel__slide--prev > .carousel__item {
	transform: scale(0.9) translate(10px);
}
.carousel__slide--active > .carousel__item {
	transform: scale(1.1);
}
</style>
