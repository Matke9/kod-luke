<script lang="ts">
	let isOpen: boolean = false;
</script>

<nav class="fixed z-50 w-full bg-white shadow-md dark:bg-gray-900">
	<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
		<div class="flex h-16 items-center justify-between">
			<!-- Logo -->
			<div class="text-accent flex-shrink-0 text-xl font-bold">
				<a href="/">Restoran</a>
			</div>

			<!-- Desktop links -->
			<div class="hidden space-x-8 text-gray-800 lg:flex dark:text-white">
				<a href="/meni" class="hover:text-accent">Meni</a>
				<a href="/o-nama" class="hover:text-accent">O nama</a>
				<a href="/galerija" class="hover:text-accent">Galerija</a>
				<a href="/lokacija" class="hover:text-accent">Lokacija</a>
				<a href="/kontakt" class="hover:text-accent">Kontakt</a>
			</div>

			<!-- Mobile menu button -->
			<div class="lg:hidden">
				<button
					on:click={() => (isOpen = !isOpen)}
					class="text-gray-800 focus:outline-none dark:text-white"
				>
					<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						{#if isOpen}
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M6 18L18 6M6 6l12 12"
							/>
						{:else}
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M4 6h16M4 12h16M4 18h16"
							/>
						{/if}
					</svg>
				</button>
			</div>
		</div>
	</div>

	<!-- Mobile dropdown menu -->
	{#if isOpen}
		<div class="space-y-2 bg-white px-4 pb-4 pt-2 shadow-md lg:hidden dark:bg-gray-900">
			<a href="/meni" class="hover:text-accent block text-gray-800 dark:text-white">Meni</a>
			<a href="/o-nama" class="hover:text-accent block text-gray-800 dark:text-white">O nama</a>
			<a href="/galerija" class="hover:text-accent block text-gray-800 dark:text-white">Galerija</a>
			<a href="/lokacija" class="hover:text-accent block text-gray-800 dark:text-white">Lokacija</a>
			<a href="/kontakt" class="hover:text-accent block text-gray-800 dark:text-white">Kontakt</a>
		</div>
	{/if}
</nav>

<style>
	.text-accent {
		color: #339989; /* možeš promeniti u boju koju koristiš za akcent */
	}
</style>
