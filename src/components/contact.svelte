<script lang="ts">
	import Saos from "saos";
</script>

<main id="contact" class="md:h-screen px-4 pt-28">
	<div class=" flex justify-center pt-14 md:pt-0 ">
		<div
			class="bg-blue-200 shadow-lg shadow-neutral-700 h-fit   px-6 border-x-4 border-y-2 border-gray-800 mx-auto container "
		>
			<div class="text-center">
				<h1 class="my-10 text-4xl">Contact</h1>
			</div>
			-
			<div class="   my-12  grid grid-cols-1 grid-rows-2 gap-6  justify-items-center md:grid-rows-1 md:grid-cols-2">
				<div class="   h-fit w-full max-w-lg  basis-1/2">
				<Saos
				animation={'fade-in 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
				animation_out={'fade-out 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
				top={200}
				bottom={200}
			>
				<div
					class=" bg-yellow-200 retro-button p-1 md:p-5  "
				>
					<div class="my-3 text-xl text-center">Get in touch</div>
					<div class="m-1 md:m-5">
						<form class="" action="https://api.web3forms.com/submit" method="POST" id="form">
							<input type="hidden" name="access_key" value="680d924c-9d31-48ed-b437-2d0bd7d6238e" />
							<input type="hidden" name="subject" value="New Submission from Web3Forms" />
							<input type="checkbox" name="botcheck" id="" style="display: none;" />

							<div class="mb-6">
								<label for="name" class="block mb-2 text-sm text-gray-600">Full Name</label>
								<input
									type="text"
									name="name"
									id="name"
									placeholder="Name"
									required
									class="w-full px-3 py-2 placeholder-gray-300 border border-gray-300 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300"
								/>
							</div>
							<div class="mb-6">
								<label for="email" class="block mb-2 text-sm text-gray-600">Email Address</label>
								<input
									type="email"
									name="email"
									id="email"
									placeholder="you@company.com"
									required
									class="w-full px-3 py-2 placeholder-gray-300 border border-gray-300 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300"
								/>
							</div>

							<div class="mb-6">
								<label for="message" class="block mb-2 text-sm text-gray-600">Your Message</label>

								<textarea
									rows="5"
									name="message"
									id="message"
									placeholder="Your Message"
									class="w-full px-3 py-2 placeholder-gray-300 border border-gray-300 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300"
									required
								/>
							</div>
							<div class="">
								<button
									type="submit"
									class="retro-button mb-1 md:mb-2 text-sm h-fit mx-auto retro-clickable w-full"
								>
									Send Message
								</button>
							</div>
							<p class="text-base text-center text-gray-400" id="result" />
						</form>
					</div>
				</div>
				</Saos>

			</div>
			<div class="   h-fit w-full max-w-lg  basis-1/2">
				<Saos
				animation={'fade-in 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
				animation_out={'fade-out 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) both'}
				top={250}
				bottom={250}
			>
				<div class=" flex flex-col bg-yellow-200  retro-button">
					<div class=" text-center my-3 text-xl">Other resources</div>
					<div class="retro-button bg-white my-2">
						<span class="block text-lg"> Email</span>
						<a class=" " href="mailto:mamma.nazim.business@gmail.com">
							<div class=" truncate">mamma.nazim.business@gmail.com</div></a
						>
					</div>
					<div class="retro-button bg-white my-2">
						<span class="block text-lg"> Upwork</span>
						<a class="truncate" href="https://www.upwork.com/freelancers/~016cd92acae26e2c3f"
							><div class=" truncate">upwork.com/freelancers/~016cd92acae26e2c3f</div></a
						>
					</div>

					<div class="retro-button bg-white my-2">
						<span class="block text-lg">LinkedIn</span>
						<a class="truncate" href="https://www.linkedin.com/in/mamma-nazim-731159274/"
							><div class=" truncate">linkedin.com/in/mamma-nazim-731159274/</div></a
						>
					</div>
					<div class="retro-button bg-white my-2">
						<span class="block text-lg">github</span>
						<a class=" " href="https://github.com/MammaNazim/"
							><div class=" truncate">github.com/MammaNazim/</div></a
						>
					</div>
				</div>
				</Saos>
			</div>
			</div>
			
		</div>
		
	</div>
</main>

<style>
	input {
		font-family: 'Roboto Condensed', sans-serif;
		font-size: medium;
	}
	textarea {
		font-family: 'Roboto Condensed', sans-serif;
		font-size: medium;
	}
	a {
		font-family: 'Roboto Condensed', sans-serif;
		font-size: large;
		color: #23a6d5;
	}

</style>
