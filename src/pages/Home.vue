<script>
import NavBar from '../components/NavBar.vue';
import Footer from '../components/Footer.vue';
import Carousel from '../components/Carousel.vue';
import gsap from 'gsap';
export default {
	components: {
		NavBar,
		Footer,
		Carousel,
	},
	setup() {
		const beforeEnter = (el) => {};
		const enter = (el) => {
			// TweenMax.to(".green", 2, {y:200, ease:Bounce.easeOut, yoyoEase:Power2.easeOut,  repeat:10, repeatDelay:0.1});
			gsap.to(el, {
				duration: 2,
				y: 50,
				// ease: Bounce.easeOut,
				// yoyoEase: Power0.easeOut,
				yoyo: true,
				repeat: -1,
				repeatDelay: 0.1,
			});

			// old
			// TweenMax.to(".class", 2, {x: 100});

			// new
			// gsap.to(".class", {duration: 2, x: 100});
		};
		const middleEnter = (el) => {
			gsap.to(el, {
				duration: 2,
				y: -30,
				// ease: Bounce.easeOut,
				// yoyoEase: Power0.easeOut,
				yoyo: true,
				repeat: -1,
				repeatDelay: 0.1,
			});
		};

		return { beforeEnter, enter, middleEnter };
	},
};
</script>

<template>
	<main>
		<section class="header lg:h-screen sm:h-3/5 mb-20">
			<NavBar />

			<header>
				<div class="grid lg:grid-cols-2 grid-cols-1 gap-2 lg:relative">
					<div class="px-16 py-20">
						<h2 class="text-4xl leading-10 font-bold"
							>For the home of <br />
							tomorrow</h2
						>
						<p class="leading-7 my-7 text-base"
							>We design sustainable furnitures. Find a piece from our large
							collection of luxurious interiors designed by professional
							interior designers.
						</p>
						<a
							class="btn lg:py-4 py-3 px-4 border-b-2 border-transparent lg:mb-0 mb-2 text-white font-bold rounded"
							href="#"
							>Explore Products</a
						>
					</div>
					<div class="grid grid-cols-3 gap-0 relative lg:visible invisible">
						<transition appear @before-enter="beforeEnter" @enter="enter">
							<div class="">
								<img
									class="w-44 absolute top-16"
									src="../assets/header1.png"
									alt=""
								/>
							</div>
						</transition>
						<transition
							appear
							@before-enter="middleBefore"
							@enter="middleEnter"
						>
							<div class="">
								<img
									class="w-44 absolute top-16"
									src="../assets/header2.png"
									alt=""
								/>
							</div>
						</transition>

						<transition appear @before-enter="beforeEnter" @enter="enter">
							<div class="">
								<img
									class="w-44 absolute top-16"
									src="../assets/header3.png"
									alt=""
								/>
							</div>
						</transition>
					</div>
				</div>
			</header>
		</section>
		<section>
			<div class="mt-40">
				<h2 class="font-bold text-4xl ml-10 leading-normal">120 +</h2>
				<h2 class="ml-10 text-lg font-medium">Branded products</h2>
				<div
					class="grid lg:grid-cols-5 grid-cols-2 justify-center items-center mx-16 my-10"
				>
					<div
						><img
							class="w-28 grid justify-center items-center"
							src="../assets/FurnitureBrands.svg"
							alt=""
					/></div>
					<div
						><img
							class="w-28 grid justify-center items-center"
							src="../assets/BassettFurniture.svg"
							alt=""
					/></div>
					<div
						><img
							class="w-28 grid justify-center items-center"
							src="../assets/Booking.svg"
							alt=""
					/></div>
					<div
						><img
							class="w-28 grid justify-center items-center"
							src="../assets/FurnitureRow.svg"
							alt=""
					/></div>
					<div
						><img
							class="grid justify-center items-center"
							src="../assets/Kronheimsfurniture.svg"
							alt=""
					/></div>
				</div>
			</div>
		</section>
		<section>
			<div class="grid lg:grid-cols-2 grid-cols-1 gap-2 relative">
				<div class="px-16 py-20 lg:order-none order-last">
					<h2 class="text-4xl leading-10 font-bold">Coffee Table</h2>
					<p class="leading-7 my-7 text-base"
						>The perfect companion for your sofa. Rigid, wooden legs attach in
						seconds to a surface sized to fit everything you need close to you.
						Available in oval or round.
					</p>
					<a
						class="btn lg:py-4 py-3 px-8 border-b-2 border-transparent lg:mb-0 mb-2 text-white font-bold rounded"
						href="#"
						>Shop Now</a
					>
				</div>
				<div class="">
					<div class="grid justify-center items-center">
						<img class="w-80" src="../assets/tablewithflower.svg" alt="" />
					</div>
				</div>
			</div>
		</section>
		<section>
			<div class="grid lg:grid-cols-2 grid-cols-1 gap-2 relative">
				<div class="">
					<div class="grid justify-center items-center">
						<img class="w-60" src="../assets/cupboard.svg" alt="" />
					</div>
				</div>
				<div class="px-16 py-20">
					<h2 class="text-4xl leading-10 font-bold">The Shelf</h2>
					<p class="leading-7 my-7 text-base"
						>A modern shelf that fits perfectly. When it comes to modularity,
						the limit is endless. Start with one shelf and add expansion units
						and add-ons to build a shelving system that works perfectly in your
						space - either in your home or office.
					</p>
					<a
						class="btn lg:py-4 py-3 px-8 border-b-2 border-transparent lg:mb-0 mb-2 text-white font-bold rounded"
						href="#"
						>Shop Now</a
					>
				</div>
			</div>
		</section>
		<section>
			<div class="flex flex-row mx-8 justify-between mt-16 mb-10">
				<h2 class="text-4xl leading-10 font-bold">Our Products</h2>
				<a href="" class="text-base product">See all</a>
			</div>
			<div class="grid lg:grid-cols-4 grid-cols-1">
				<div class="grid justify-center items-center">
					<img class="w-56" src="../assets/product1.svg" alt="" />
					<div class="text-center product">Chairs</div>
				</div>
				<div class="grid justify-center items-center">
					<img class="w-56" src="../assets/product2.svg" alt="" />
					<div class="text-center product">Tables</div>
				</div>
				<div class="grid justify-center items-center">
					<img class="w-56" src="../assets/product3.svg" alt="" />
					<div class="text-center product">Sofas</div>
				</div>
				<div class="grid justify-center items-center">
					<img class="w-56" src="../assets/product4.svg" alt="" />
					<div class="text-center product">Cupboards</div>
				</div>
			</div>
		</section>
		<section>
			<div class="grid lg:grid-cols-2 grid-flow-row gap-2 relative">
				<div class="lg:visible invisible">
					<div class="grid justify-center items-center -mr-24 mt-14">
						<img class="lg:w-96 w-0" src="../assets/longtable.svg" alt="" />
					</div>
				</div>
				<div class="lg:pr-14 pr-0 py-20 px-4">
					<h2 class="text-2xl leading-10 font-medium"
						>Find your ideal <br />
						interior design.</h2
					>
					<p class="leading-7 my-7 text-sm"
						>Styling a room is an art, from mixing and matching wood to figuring
						out which coffee tables go best with which sectionals. Be inspired.
					</p>
					<a
						class="btn lg:py-4 py-3 px-8 border-b-2 border-transparent lg:mb-0 mb-2 text-white font-bold rounded"
						href="#"
						>Discover</a
					>
					<div class="grid justify-center items-center mt-7">
						<img class="w-5/6" src="../assets/readingtable.svg" alt="" />
					</div>
				</div>
			</div>
		</section>
		<section>
			<div class="my-20 testimonials py-10">
				<h2 class="text-white text-3xl leading-10 font-bold mx-10"
					>What Our Clients Say</h2
				>
				<Carousel />
			</div>
		</section>
		<section>
			<div class="grid justify-center items-center px-40 my-20">
				<h3 class="text-center lg:text-3xl text-lg leading-10 font-semibold"
					>Subscribe to our Newsletter</h3
				>
				<p class="text-center text-sm"
					>Get a 20% OFF (plus the latest furniture news and <br />
					product launches) just by subscribing to our newsletter.</p
				>
				<div class="flex lg:flex-row flex-col justify-center items-center">
					<input
						type="email"
						class="m-8 border-warmGray-300 focus:outline-none focus:border-rose-200 border-2 py-4 px-10 rounded"
						placeholder="Enter your email"
					/>
					<a
						class="btn lg:py-4 py-3 px-12 border-b-2 border-transparent lg:mb-0 mb-2 text-white font-bold rounded"
						href="#"
						>Subscribe</a
					>
				</div>
			</div>
		</section>
		<Footer />
	</main>
</template>

<style scoped>
.header {
	background-color: #f6eddd;
	/* height: 100vh; */
}
.btn {
	background-color: #623b1c;
}
.btn:hover {
	background: linear-gradient(270deg, #bfa1a7 0%, #fad088 100%);
}
.testimonials {
	background-color: #caad8c;
}
.product {
	color: #623b1c;
}
</style>
