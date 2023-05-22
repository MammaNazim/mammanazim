<script lang="ts">
	import Saos from 'saos';
</script>

<main id="about" class=" ">
	<div class="main-div flex w-screen justify-center mt-40 justify-items-center">
		<div
			class=" mx-4 container px-2 md:px-10 flex flex-col bg-blue-200 shadow-lg shadow-neutral-700 border-x-4 border-y-2 text-xs sm:text-sm md:text-base border-gray-800"
		>
			<div class=" text-4xl mt-10 mx-auto">About me</div>
			<div class="self-start mx-2 md:mx-10 my-6 sm:my-12">
				<Saos animation={'slide-in-right 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
					<div class="retro-button bg-yellow-200">
						I'm a front-end developer with a passion for solving problems and creating visually
						appealing websites.
					</div>
				</Saos>
			</div>

			<div class="self-end mx-2 md:mx-10 my-6 sm:my-12">
				<Saos animation={'slide-in-left 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
					<div class="retro-button bg-yellow-200">
						I take great pride in my ability to create responsive and visually appealing designs.
						Whether it's crafting an intuitive user experience or implementing eye-catching visuals.
					</div>
				</Saos>
			</div>

			<div class="self-start mx-2 md:mx-10 my-6 sm:my-12">
				<Saos animation={'slide-in-right 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
					<div class="retro-button bg-yellow-200">
						if you're looking for a front-end developer who can make your project stand out, let's
						collaborate! Together, Let's bring your vision to life, one line of code at a time!
					</div>
				</Saos>
			</div>
		</div>
	</div>
</main>

<style>
	@keyframes -global-slide-in-left {
		0% {
			transform: translateX(-20px);
			opacity: 0;
		}
		100% {
			transform: translateX(0);
			opacity: 1;
		}
	}

	@keyframes -global-slide-in-right {
		0% {
			transform: translateX(20px);
			opacity: 0;
		}
		100% {
			transform: translateX(0);
			opacity: 1;
		}
	}
	@media screen and (min-width: 768px) {
		@keyframes -global-slide-in-right {
			0% {
				transform: translateX(200px);
				opacity: 0;
			}
			100% {
				transform: translateX(0);
				opacity: 1;
			}
		}
		@keyframes -global-slide-in-left {
			0% {
				transform: translateX(-200px);
				opacity: 0;
			}
			100% {
				transform: translateX(0);
				opacity: 1;
			}
		}
	}
	.retro-button {
		max-inline-size: 425px;

		text-align: center;
	}
	.main-div {
		margin-top: 5rem;
	}
</style>
