<script lang="ts">
	import Saos from 'saos';

	let projects = [
		{
			title: 'Gym website',
			description: 'Description of Project 1',
			image: 'src/images/Screenshot_2023-05-23_08-06-16.png',
			demoLink: 'https://example.com/demo1',
			codeLink: 'https://github.com/your-username/project1'
		},
		{
			title: 'Project 2',
			description: 'Description of Project 2',
			image: 'src/images/Screenshot_2023-05-23_08-06-16.png',
			demoLink: 'https://example.com/demo2',
			codeLink: 'https://github.com/your-username/project2'
		},

	];
</script>

<main id="projects" class=" pt-32">
	<div class="mx-4 lg:mx-40 main-div center flex justify-center h-screen justify-items-center">
		<div
			class="bg-blue-200 shadow-lg shadow-neutral-700 h-fit my-auto border-x-4 border-y-2 border-gray-800 mx-auto container"
		>
			<div class=" text-center text-4xl my-10">Projects</div>
			<div
				class=" py-20 grid grid-cols-1 items-end md:grid-cols-2 xl:grid-cols-2 mx-5 md:mx-12 gap-x-2 gap-y-6 md:gap-6 my-10 justify-items-center"
			>
				{#each projects as project}
					<Saos
						animation={'fade-in 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
						animation_out={'fade-out 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
						top={250}
						bottom={250}
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
											<img class="h-6 my-auto" src="src/images/play.png" alt="" />
											<div class=" my-auto text-sm w-10 lg:text-base">Demo</div></a
										></button
									>
									<button class="label-btn bg-pink-200 w-20 retro-button-clickable px-1 mx-0.5"
										><a href={project.codeLink} class="px-1 flex">
											<img class="h-4 pr-1.5 pl-1 my-auto" src="src/images/code.png" alt="" />
											<div class=" my-auto text-sm w-10 lg:text-base">Code</div></a
										></button
									>
								</div>
							</div>
							<div class="window-body">
								<div class="image">
								<img class="" src={project.image} alt={project.title} />
								<div class="image-overlay transition-all">
									<div class="image-description  text-xl text-white">{project.description}</div>
								</div>
							</div>
							</div>
						</div>
					</Saos>
				{/each}
			</div>
		</div>
	</div>
</main>

<style>	
	img {
		
		display: block;
	}
	.image{
		position: relative;
		width: 100%;
	}
	.image-overlay{
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
		.image-overlay:hover{
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
</style>
