<script lang="ts">
	let path = 'home';
	function home() {
		path = 'home';
	}
	function about() {
		path = 'about';
	}
	function projects() {
		path = 'projects';
	}
	function contact() {
		path = 'contact';
	}
</script>

<header
	class=" navbar z-50 fixed w-full bg-blue-200 shadow shadow-neutral-700 border-b-2 border-gray-800 py-3"
>
	<nav class="navbar-element flex justify-center lg:justify-around">
		<div class="home-button">
			{#if path === 'home'}
				<a
					on:click={home}
					href="/"
					class="retro-button clicked retro-clickable text-center flex items-center"
				>
					<img src="src/images/folder-open.png" class="image h-6 w-6 mr-2" alt="" />
					<span>Home</span>
				</a>
			{:else}
				<a
					on:click={home}
					href="/"
					class="retro-button retro-clickable text-center flex items-center"
				>
					<img src="src/images/folder.png" class="image h-6 w-6 mr-2" alt="" />
					<span>Home</span>
				</a>
			{/if}
		</div>
		<div class="navbar-element other-buttons flex space-x-2 sm:space-x-6">
			{#if path === 'about'}
				<a
					on:click={about}
					href="#about"
					class="retro-button clicked retro-clickable text-center flex items-center"
				>
					<img src="src/images/folder-open.png" class="image h-6 w-6 mr-2" alt="" />
					<span>About me</span></a
				>
			{:else}
				<a
					on:click={about}
					href="#about"
					class="retro-button retro-clickable text-center flex items-center"
				>
					<img src="src/images/folder.png" class="image h-6 w-6 mr-2" alt="" />
					<span>About me</span></a
				>
			{/if}
			{#if path === 'projects'}
				<a
					on:click={projects}
					href="#projects"
					class="retro-button clicked retro-clickable text-center flex items-center"
				>
					<img src="src/images/folder-open.png" class="image h-6 w-6 mr-2" alt="" />
					<span>Projects</span></a
				>
			{:else}
				<a
					on:click={projects}
					href="#projects"
					class="retro-button retro-clickable flex items-center"
				>
					<img src="src/images/folder.png" class="image h-6 w-6 mr-2" alt="" />
					<span>Projects</span></a
				>
			{/if}
			{#if path === 'contact'}
				<a
					on:click={contact}
					href="#contact"
					class="retro-button clicked retro-clickable text-center flex items-center"
				>
					<img src="src/images/folder-open.png" class="image h-6 w-6 mr-2" alt="" />
					<span>Contact</span></a
				>
			{:else}
				<a
					on:click={contact}
					href="#contact"
					class="retro-button retro-clickable flex items-center"
				>
					<img src="src/images/folder.png" class="image h-6 w-6 mr-2" alt="" />
					<span>Contact</span></a
				>
			{/if}
		</div>
	</nav>
</header>

<style>
	@media (max-width: 530px) {
		.home-button {
			margin-right: 0.5rem;
		}
		.other-buttons {
			margin-right: 0.5rem;
		}
		.navbar-element {
			font-size: 70%;
		}
		.retro-button {
			padding-right: 5px;
			padding-left: 5px;
			padding-top: 5px;
			padding-bottom: 5px;
			height: 4rem;
		}
	}
	@media (max-width: 475px) {
		.navbar-element {
			font-size: 80%;
		}
	}
	@media (max-width: 768px) {
		.image {
			display: none;
		}
		.navbar-element {
			font-size: 85%;
		}
	}
	.home-button {
		margin-right: 1rem;
		margin-left: 1rem;
	}
	.other-buttons {
		margin-right: 1rem;
	}
	.clicked {
		background-color: #f9a8d4;
		box-shadow: 0px 0px #404040;
		transform: translateX(5px) translateY(2px);
	}
</style>
