<script lang="ts">
	import Saos from 'saos';
</script>

<main id="about" class="pt-20 ">
	<div class="main-div flex  justify-center h-auto sm:h-screen justify-items-center">
		<div
			class=" my-auto mx-4  container px-2 md:px-10 flex flex-col bg-blue-200 shadow-lg shadow-neutral-700 border-x-4 border-y-2 text-xs sm:text-sm md:text-base border-gray-800"
		>
			<div class=" text-4xl my-10 mx-auto">About me</div>
			<div class="self-start mx-6 md:mx-10 my-2 sm:my-6">
				<Saos animation={'slide-in-right 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}				
				animation_out={'slide-out-right 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'} 
				top={250}
				bottom={250}>
					<div class="about retro-button bg-yellow-200">
						I'm a front-end developer with a passion for solving problems and creating visually
						appealing websites.
					</div>
				</Saos>
			</div>

			<div class="self-end mx-6 md:mx-10 my-2 sm:my-6">
				<Saos animation={'slide-in-left 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'} 
				animation_out={'slide-out-left 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'} 
				top={250}
				bottom={250}>
					<div class="about retro-button bg-yellow-200">
						I take great pride in my ability to create responsive and visually appealing designs.
						Whether it's crafting an intuitive user experience or implementing eye-catching visuals.
					</div>
				</Saos>
			</div>

			<div class="self-start mx-6 md:mx-10 my-2 sm:my-6">
				<Saos animation={'slide-in-right 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'} 				
				animation_out={'slide-out-right 0.5s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'} 
				top={250}
				bottom={250}>
					<div class="about retro-button bg-yellow-200">
						if you're looking for a front-end developer who can make your project stand out, let's
						collaborate! Together, Let's bring your vision to life, one line of code at a time!
					</div>
				</Saos>
			</div>
		</div>
	</div>
	<div class="flex arrow-div my-6">
		<a
			href="#about"
			class="retro-button retro-clickable w-24 h-24 rounded-full mx-auto border-4 border-black"
		>
			<img src="src/images/arrow.png" alt="down arrow" class="arrow" />
		</a>
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
	@keyframes -global-slide-out-left {
		0% {
			transform: translateX(0px);
			opacity: 1;
		}
		100% {
			transform: translateX(-20px);
			opacity: 0;
		}
	}

	@keyframes -global-slide-out-right {
		0% {
			transform: translateX(0);
			opacity: 1;
		}
		100% {
			transform: translateX(20px);
			opacity: 0;
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
	@media screen and (min-width: 768px) {
		@keyframes -global-slide-out-right {
			0% {
				transform: translateX(0);
				opacity: 1;
			}
			100% {
				transform: translateX(200px);
				opacity: 0;
			}
		}
		@keyframes -global-slide-out-left {
			0% {
				transform: translateX(0);
				opacity: 1;
			}
			100% {
				transform: translateX(-200px);
				opacity: 0;
			}
		}
	}
	@media (max-width: 630px) {
    .about {
        width: 15rem;
    }
}	
@keyframes slide-left {
		0% {
			transform: translateX(0px);
		}
		50% {
			transform: translateX(-10px);
		}
		100% {
			transform: translateX(0px);
		}
	}

	@media screen and (min-width: 768px) {
		@keyframes slide-left {
			0% {
				transform: translateX(20px);
			}

			50% {
				transform: translateX(0);
			}
			100% {
				transform: translate(20px);
			}
		}

	}
	@keyframes slide-right {
		0% {
			transform: translateX(0px);
		}
		50% {
			transform: translateX(10px);
		}
		100% {
			transform: translateX(0px);
		}
	}

	@media screen and (min-width: 768px) {
		@keyframes slide-right {
			0% {
				transform: translateX(-20px);
			}

			50% {
				transform: translateX(0);
			}
			100% {
				transform: translate(-20px);
			}
		}

	}
.self-start{
	animation: slide-left 1.5s infinite;

}
.self-end{
	animation: slide-right 1.5s infinite;
}
	.container{
		max-width: 900px;

	}
	.retro-button {
		max-inline-size: 425px;

		text-align: center;
	}
	.main-div {
		margin-top: 5rem;
	}


</style>
