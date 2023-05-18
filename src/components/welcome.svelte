<script lang="ts">
	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';
	import { fade } from 'svelte/transition';

	let visible = false;
	let currentIndex = 0;
	let currentString = '';

	const stringsArray = ['programmer', 'freelancer', 'cat lover', 'nerd'];

	function changeString() {
		currentString = stringsArray[currentIndex];
		currentIndex = (currentIndex + 1) % stringsArray.length;
	}

	onMount(() => {
		visible = true;
		const interval = setInterval(changeString, 2000);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<main class=" w-full mx-auto">
	{#if visible}
		<div transition:fade={{ duration: 1000 }} class="h-screen flex flex-row justify-center">
			<div class="flex flex-col  justify-end ">
				<div class="silly-cat mx-auto w-36" />
				<div
					class="mx-auto  px-10 flex bg-blue-200 shadow-lg shadow-neutral-700 border-x-4 border-y-2 border-gray-800 justify-start items-center"
				>
					<div class=" px-auto py-6 h-full flex justify-evenly flex-col">
						<span class="text-4xl font-light py-10"> Hello, my name is </span>
						<span class="retro-button font-bold text-xl bg-yellow-200 border-black">
							MAMMA NAZIM</span
						>
						<span class="text-4xl font-light py-6"> And </span>
						<div class="retro-button font-light bg-yellow-200 flex text-sm mb-6">
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
				<a href="/" class="retro-button retro-clickable w-16 h-16 rounded-full mx-auto my-4 lg:my-6  border-4 border-black">
				
				<img 
					src="https://drive.google.com/uc?export=download&id=1ryjKQeJ-4faTvxIs8ABCFhjDl7kmvv2d"
					alt="down arrow"
					class="arrow"> 
				</a>
			</div>

		</div>
	{/if}
</main>

<style>
	.silly-cat {
		background-image: url('https://drive.google.com/uc?export=download&id=19JfsejCScqvw7KlqjUF0mAjQKXBN4XVX');
		height: 107px;
		background-size: 144px;
	}
</style>
