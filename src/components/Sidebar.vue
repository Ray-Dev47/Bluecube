<template>
	<!-- give the sidebar z-50 class so its higher than the navbar if you want to see the logo -->
	<!-- you will need to add a little "X" button next to the logo in order to close it though -->
	<div
		class="w-1/2 md:w-1/3 lg:w-64 fixed md:top-0 md:left-0 h-screen lg:block bg-gray-100 border-r z-30"
		:class="sideBarOpen ? '' : 'hidden'"
		id="main-nav"
	>
		<div class="w-full h-20 border-b flex px-4 items-center mb-8">
			<img class="w-8" src="@/assets/bluecube-logo.png" alt="bluecubelogo" />
			<p class="font-bold text-xl text-primary pl-2">bluecube</p>
		</div>
		<div class="mb-4 px-4">
			<!-- <p class="pl-4 text-sm font-semibold mb-1">MAIN</p> -->
			<div
				class="w-full flex items-center text-gray-200 h-10 pl-4 bg-gray-200 hover:bg-gray-200 hover:text-primary hover:border rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="h-6 w-6 text-gray-800   mr-2 feather feather-home"
				>
					<path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path>
					<polyline points="9 22 9 12 15 12 15 22"></polyline>
				</svg>
				<span class="text-gray-700 text-sm hover:text-primary">Dashboard</span>
			</div>
			<div
				class="w-full flex items-center text-gray-200 h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="feather h-6 w-6 text-gray-800   mr-2 feather-mail"
				>
					<path
						d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
					></path>
					<polyline points="22,6 12,13 2,6"></polyline>
				</svg>
				<span class="text-gray-700 text-sm">Message</span>
			</div>
		</div>

		<div class="mb-4 px-4">
			<p class="pl-4 text-sm font-semibold mb-1">SHARE</p>
			<div
				class="w-full flex items-center text-blue-400 h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="h-6 w-6 text-gray-800 fill-current mr-2 feather feather-bar-chart-2"
				>
					<line x1="18" y1="20" x2="18" y2="10"></line>
					<line x1="12" y1="20" x2="12" y2="4"></line>
					<line x1="6" y1="20" x2="6" y2="14"></line>
				</svg>
				<span class="text-gray-700 text-sm">Ranking</span>
			</div>
			<div
				class="w-full flex items-center text-blue-400 h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="icon h-6 w-6 text-gray-800 fill-current mr-2 icon-tabler icon-tabler-tournament"
					width="44"
					height="44"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="#2c3e50"
					fill="none"
					stroke-linecap="round"
					stroke-linejoin="round"
				>
					<path stroke="none" d="M0 0h24v24H0z" fill="none" />
					<path d="M5 4h4a1 1 0 0 1 1 1v4a1 1 0 0 1 -1 1h-4" />
					<path d="M5 14h4a1 1 0 0 1 1 1v4a1 1 0 0 1 -1 1h-4" />
					<path d="M10 7h4a1 1 0 0 1 1 1v8a1 1 0 0 1 -1 1h-4" />
					<line x1="15" y1="12" x2="20" y2="12" />
				</svg>
				<span class="text-gray-700 text-sm">Challenge</span>
			</div>

			<div
				class="w-full flex items-center text-blue-400 h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="icon h-6 w-6 text-gray-800 fill-current mr-2 icon-tabler icon-tabler-confetti"
					width="44"
					height="44"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="#2c3e50"
					fill="none"
					stroke-linecap="round"
					stroke-linejoin="round"
				>
					<path stroke="none" d="M0 0h24v24H0z" fill="none" />
					<path d="M4 5h2" />
					<path d="M5 4v2" />
					<path d="M11.5 4l-.5 2" />
					<path d="M18 5h2" />
					<path d="M19 4v2" />
					<path d="M15 9l-1 1" />
					<path d="M18 13l2 -.5" />
					<path d="M18 19h2" />
					<path d="M19 18v2" />
					<path
						d="M14 16.518l-6.518 -6.518l-4.39 9.58a1.003 1.003 0 0 0 1.329 1.329l9.579 -4.39z"
					/>
				</svg>
				<span class="text-gray-700 text-sm">Party</span>
			</div>

			<div
				class="w-full flex items-center text-blue-400 h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-6 w-6 text-gray-800 fill-current mr-2 icon icon-tabler icon-tabler-line"
					width="44"
					height="44"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="#2c3e50"
					fill="none"
					stroke-linecap="round"
					stroke-linejoin="round"
				>
					<path stroke="none" d="M0 0h24v24H0z" fill="none" />
					<circle cx="6" cy="18" r="2" />
					<circle cx="18" cy="6" r="2" />
					<line x1="7.5" y1="16.5" x2="16.5" y2="7.5" />
				</svg>
				<span class="text-gray-700 text-sm">Connect</span>
			</div>

			<div
				class="w-full flex items-center text-blue-400 h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="h-6 w-6 text-gray-800 fill-current mr-2  feather feather-wind"
				>
					<path
						d="M9.59 4.59A2 2 0 1 1 11 8H2m10.59 11.41A2 2 0 1 0 14 16H2m15.73-8.27A2.5 2.5 0 1 1 19.5 12H2"
					></path>
				</svg>
				<span class="text-gray-700 text-sm">Parade</span>
			</div>

			<div
				class="w-full flex items-center text-blue-400 h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="h-6 w-6 text-gray-800 fill-current mr-2 feather feather-users"
				>
					<path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path>
					<circle cx="9" cy="7" r="4"></circle>
					<path d="M23 21v-2a4 4 0 0 0-3-3.87"></path>
					<path d="M16 3.13a4 4 0 0 1 0 7.75"></path>
				</svg>
				<span class="text-gray-700 text-sm">Group</span>
			</div>
		</div>
	</div>
</template>

<script>
// import { mapState } from 'vuex'

export default {
	name: 'Sidebar',
	// computed: {
	//     ...mapState(['sideBarOpen'])
	// }
};
</script>
