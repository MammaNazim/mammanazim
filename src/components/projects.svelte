<script lang="ts">
	import Saos from 'saos';
	
	import play from "$lib/images/play.png"
	import code from "$lib/images/code.png"
	import gymthumbnail from "$lib/images/gymthumbnail.png"
	import arrow from "$lib/images/arrow.png"

	let projects = [
		{
			title: 'Gymforce',
			description: 'Gymforce is a visually captivating website designed to inspire fitness enthusiasts. It offers a great browsing experience. With its sleek design and responsive layout, users can easily navigate and schedule workouts across devices.',
			thumbnail: gymthumbnail,
			demoLink: 'https://gymforce.vercel.app/',
			codeLink: 'https://github.com/MammaNazim/gymforce'
		},

	];
</script>

<main id="projects" class=" md:h-screen pt-32">
	<div class="mx-4 lg:mx-40 main-div center flex justify-center justify-items-center">
		<div
			class="bg-blue-200 shadow-lg shadow-neutral-700 h-fit my-auto border-x-4 border-y-2 border-gray-800 mx-auto container"
		>
			<div class=" text-center text-4xl my-10">Projects</div>
			<div
				class=" py-20 grid grid-cols-1 items-end md:grid-cols-1 xl:grid-cols-1 mx-5 md:mx-12 gap-x-2 gap-y-6 md:gap-6 my-10 justify-items-center"
			>
				{#each projects as project}
					<Saos
						animation={'fade-in 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
						animation_out={'fade-out 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
						top={200}
						bottom={200}
					>
						<div class="window">
							<div class="title-bar bg-none bg-blue-300 flex justify-between">
								<div
									class="title-bar-text pl-3 text-sm lg:text-lg text-black sm:basis-2/4 basis-2/5"
								>
									{project.title}
								</div>
								<div class="title-bar-controls sm:basis-2/4 basis-3/5 justify-end">
									<button class="label-btn w-20 retro-button-clickable bg-pink-200 px-1 mx-0.5"
										><a href={project.demoLink} class="px-1 flex">
											<img class=" h-6 my-auto" src={play} alt="" />
											<div class=" my-auto text-sm w-10 lg:text-base">Demo</div></a
										></button
									>
									<button class="label-btn bg-pink-200 w-20 retro-button-clickable px-1 mx-0.5"
										><a href={project.codeLink} class="px-1 flex">
											<img class="h-4 pr-1.5 pl-1 my-auto" src={code} alt="" />
											<div class=" my-auto text-sm w-10 lg:text-base">Code</div></a
										></button
									>
								</div>
							</div>
							<div class="window-body">
								<div class="image">
									<img class=" aspect-video" src={project.thumbnail} alt={project.title} />
									<div class="image-overlay transition-all">
										<div class="image-description text-sm sm:text-base md:text-2xl text-white text-center px-6">{project.description}</div>
									</div>
								</div>
							</div>
						</div>
					</Saos>
				{/each}
			</div>
		</div>
	</div>
	<div class="flex arrow-div my-6">
		<a
			href="#contact"
			class="retro-button retro-clickable w-24 h-24 rounded-full mx-auto border-4 border-black"
		>
			<img src={arrow} alt="down arrow" class="arrow" />
		</a>
	</div>
</main>

<style>

	img {
		display: block;
	}
	.image {
		position: relative;
		max-width: 650px;
	}
	.image-overlay {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0, 0, 0, 0.6);
		display: flex;
		font-family: 'Roboto Condensed', sans-serif;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		opacity: 0;

	}
	.image-overlay:hover {
		opacity: 1;
	}
	.image-overlay > * {
		transform: translateY(20px);
		transition: transform 0.25s;
	}
	.image-overlay:hover > * {
		transform: translateY(0);
	}
	@keyframes -global-fade-in {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	@keyframes -global-fade-out {
		0% {
			opacity: 1;
		}
		100% {
			opacity: 0;
		}
	}
	@media screen and (max-width: 839px) {
		.arrow-div {
			display: none;
		}
	}
</style>
