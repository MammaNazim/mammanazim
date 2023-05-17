<script lang="ts">
	import { onMount } from 'svelte';
    

	let currentIndex = 0;
	let currentString = '';

	const stringsArray = ['programmer', 'freelancer', 'cat lover', 'fitness enthusiast', 'gamer'];

	function changeString() {
		currentString = stringsArray[currentIndex];
		currentIndex = (currentIndex + 1) % stringsArray.length;
	}

	onMount(() => {
		const interval = setInterval(changeString, 3000);

		return () => {
			clearInterval(interval);
		};
	});

    
</script>
<main class="h-screen flex ">
<div class="h-4/6 flex border-y-black border my-auto w-full justify-start items-center ">
	<div class="   h-full flex justify-evenly  flex-col">
		<div class=" text-xl">
			Hello, im <span>Mamma Nazim</span>
		</div>
		<div>
			im a <span>{currentString}</span>
		</div>
	</div>
</div>
</main>