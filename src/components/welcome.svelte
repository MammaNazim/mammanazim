<script lang="ts">
	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';
	import { fade } from 'svelte/transition';
	
	import orangeCat from "$lib/images/orangecat.gif"
	import svelte from "$lib/images/svelte.png"
	import tailwind from "$lib/images/tailwindcss.png"
	import typescript from "$lib/images/typescript.png"
	import git from "$lib/images/git.png"
	import arrow from "$lib/images/arrow.png"
	
	let visible = false;
	let currentIndex = 0;
	let currentString = '';
	let rainbowText = '';
	let isActive = false;

	const stringsArray = ['programmer', 'freelancer', 'cat lover', 'nerd'];
	
	function changeString() {
		currentString = stringsArray[currentIndex];
		currentIndex = (currentIndex + 1) % stringsArray.length;
	}
	function handleClick() {
		isActive = !isActive;
	}
	onMount(() => {
		visible = true;
		const interval = setInterval(changeString, 2000);

		return () => {
			clearInterval(interval);
		};
	});
	onMount(() => {
		const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet'];
		let index = 0;

		const interval = setInterval(() => {
			rainbowText = colors[index];
			index = (index + 1) % colors.length;
		}, 500);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<main class="w-full mx-auto">
				<div class="parent-div flex flex-col justify-center lg:h-screen  pt-14 ">

	{#if visible}
				<div class="main-div flex flex-col">
					<div class="flex flex-wrap lg:gap-12 gap-y-44  justify-center items-end first-card">
						<div
							transition:fly={{ delay: 100, y: -100, duration: 2000 }}
							class=" my-auto flex justify-center flex-col lg:max-h-screen"
						>
							<img src={orangeCat} class="w-36" alt="orang" />
							<div
								class="  px-10 flex bg-blue-200 shadow-lg shadow-neutral-700 border-x-4 border-y-2 border-gray-800 h-80"
							>
								<div class="px-auto py-4 h-full flex justify-evenly flex-col">
									<span class="text-4xl font-light py-6"> Hello, my name is </span>
									<span class="retro-button font-bold text-xl bg-yellow-200 border-black">
										MAMMA NAZIM</span
									>
									<span class="text-4xl font-light py-6"> And </span>
									<div class="retro-button font-light pb-6 bg-yellow-200 flex text-sm mb-6">
										I'm a
										{#key currentString}
											<div
												class="absolute pl-20"
												in:fly={{ y: -20, duration: 500 }}
												out:fly={{ y: 20, duration: 500 }}
											>
												{currentString}
											</div>
										{/key}
									</div>
								</div>
							</div>
						</div>

						<div
							transition:fly={{ delay: 1000, y: 100, duration: 2000 }}
							class=" my-40 mx-4 md:max-h-screen flex justify-center flex-col"
						>
							<div
								class="skills px-10 grid grid-rows-4 bg-blue-200 shadow-lg shadow-neutral-700 border-x-4 border-y-2 border-gray-800"
							>
								<div class=" row-span-1">
									<span class="text-3xl font-light my-2 table">
										Technologies used<strong>:</strong></span
									>
									<div
										class="retro-button bg-yellow-200 grid-element grid grid-cols-2 sm:grid-cols-4 gap-x-2"
									>
										<div class="transition-all hover:text-orange-500 skill-individual">
											<img class="skill-img mx-auto" src={svelte} alt="" />
											<div class=" font-bold text-center">Svelte</div>
										</div>
										<div class="transition-all hover:text-blue-500 skill-individual">
											<img class="skill-img mx-auto" src={typescript} alt="" />
											<div class=" font-bold text-center">Typescript</div>
										</div>
										<div class="transition-all hover:text-cyan-400 skill-individual">
											<img class="skill-img mx-auto" src={tailwind} alt="" />
											<div class=" font-bold text-center">Tailwind</div>
										</div>
										<div class="transition-all hover:text-orange-500 skill-individual">
											<img class="skill-img mx-auto" src={git} alt="" />
											<div class=" font-bold text-center">Git</div>
										</div>
									</div>
								</div>
								<div class="flex flex-col justify-end row-span-3">
									<div class="">
										{#if isActive}
											<div
												class="sm:w-80 w-48 retro sm:text-base text-xs mx-auto text-center"
												in:fly={{ duration: 300, y: 85 }}
											>
												i can bring your website ideas to <div
													class="sm:pb-6 pb-2 sm:mt-9 mt-3 rainbow"
													in:fade={{ delay: 1000, duration: 300 }}
												>
													LIFE
												</div>
											</div>
										{/if}
									</div>
									<div class="mx-auto">
										<svg
											class="my-1"
											class:active={isActive}
											width="76px"
											height="76px"
											viewBox="0 0 76 76"
											xmlns="http://www.w3.org/2000/svg"
										>
											<path id="greyshadow" d="M8 8h68v68h-68z" fill="#BFBFBF" />
											<path id="blackborder" d="M4 4h68v68h-68z" fill="#000" />
											<path id="background" d="M4 4h64v64h-64z" fill="#FFC07C" />
											<path
												id="borderlefttop"
												d="M4 0h64M0 4v64"
												stroke="#DE5917"
												stroke-width="8"
											/>
											<path
												id="rivets"
												d="M8 8h4v4h-4zM60 60h4v4h-4zM8 60h4v4h-4zM60 8h4v4h-4z"
												fill="#000"
											/>
											<path
												id="questionshadow"
												d="M24 20h4v-4h20v4h4v16h-8v8h-8v-8h4v-4h4v-12h-12v12h-8zM36 52h8v8h-8z"
												fill="#000"
											/>
											<path
												id="question"
												d="M20 16h4v-4h20v4h4v16h-8v8h-8v-8h4v-4h4v-12h-12v12h-8zM32 48h8v8h-8z"
												fill="#DE5917"
											/>
										</svg>
									</div>
									<button
										class="retro-button mb-6 text-sm h-fit mx-auto retro-clickable"
										on:click|once={handleClick}
									>
										what can i do?
									</button>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div class="flex arrow-div my-6">
					<a
						href="#about"
						class="retro-button retro-clickable w-24 h-24 rounded-full mx-auto border-4 border-black"
					>
						<img src={arrow} alt="down arrow" class="arrow" />
					</a>
				</div>
	{/if}	
		</div>

</main>

<style>
	@media (max-width: 850px) {
		.parent-div {
			padding-top: 25vh;
		}
	}
	@media screen and (min-height: 850px) {
		.main-div {
			margin-top: auto;
			margin-bottom: auto;
		}
	}
	@media screen and (max-width: 839px) {
		.arrow-div {
			display: none;
		}

	}

	.arrow {
		transform: scale(1.5);
	}
	.main-div {
		margin-top: auto;
	}

	.skills {
		height: 27rem;
	}
	.skill-img {
		height: 2rem;
		width: 2rem;
	}
	.grid-element {
		font-size: 8px;
		padding: 6px;
	}
	.skill-individual:hover {
		transform: scale(1.15);
	}

	svg.active > #rivets,
	svg.active > #question {
		fill: #000;
	}
	svg.active > #borderlefttop {
		stroke: #000;
	}
	svg.active > #background,
	svg.active > #question,
	svg.active > #questionshadow {
		fill: #de5917;
		transition: fill 0s;
	}

	@keyframes jump {
		50% {
			transform: translatey(-2.5rem);
		}
		to {
			transform: translatey(0);
		}
	}
	svg.active {
		animation: jump 0.4s;
	}

</style>
