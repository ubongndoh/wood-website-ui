<script></script>

<template>
	<header
		class="lg:px-16 px-6 bg-transparent flex flex-wrap items-center lg:py-6 py-2"
	>
		<div class="flex w-2/6 justify-between items-center">
			<a href="#">
				<div class="flex flex-none justify-between items-center">
					<span class="mx-4 font-bold text-2xl title1">Woods</span>
				</div>
			</a>
		</div>

		<label for="menu-toggle" class="cursor-pointer ml-48 lg:hidden block"
			><svg
				class="fill-current text-gray-900"
				xmlns="http://www.w3.org/2000/svg"
				width="20"
				height="20"
				viewBox="0 0 20 20"
			>
				<title>menu</title>
				<path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path></svg
		></label>
		<input class="hidden" type="checkbox" id="menu-toggle" />

		<div class="hidden lg:flex lg:items-center lg:w-auto w-full" id="menu">
			<nav class="flex flex-row">
				<ul
					class="lg:flex flex-1 lg:w-5/6 items-center justify-between text-sm text-gray-700 pt-4 lg:pt-0"
				>
					<li
						><a
							class="lg:p-4 py-3 px-0 block border-b-2 border-transparent lg:hover:border-rose-800"
							href="#"
							>Home</a
						></li
					>
					<li
						><a
							class="lg:p-4 py-3 px-0 block border-b-2 border-transparent lg:hover:border-rose-800"
							href="#"
							>Products</a
						></li
					>
					<li
						><a
							class="lg:p-4 py-3 px-0 block border-b-2 border-transparent lg:hover:border-rose-800"
							href="#"
							>Discover</a
						></li
					>
					<li
						><a
							class="lg:p-4 py-3 px-0 block border-b-2 border-transparent lg:hover:border-rose-800 lg:mb-0 mb-2"
							href="#"
							>Contact</a
						></li
					>
				</ul>
				<ul
					class="lg:flex items-center justify-between text-sm text-gray-700 block ml-60"
				>
					<li class="lg:p-4 p-0 py-3 px-2 cursor-pointer"
						><img src="../assets/Search.svg" alt=""
					/></li>
					<li class="lg:p-4 p-0 py-3 px-2 cursor-pointer"
						><img src="../assets/Bag.svg" alt=""
					/></li>
				</ul>
			</nav>
		</div>
	</header>
</template>

<style scoped>
#menu-toggle:checked + #menu {
	display: block;
	/* cursor: pointer; */
}

.title1 {
	color: #623b1c;
}
.btn {
	background-color: #623b1c;
}
</style>
