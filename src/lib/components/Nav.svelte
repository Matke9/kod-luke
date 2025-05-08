<script lang="ts">
	let isOpen: boolean = false;
</script>

<nav class="absolute z-50 w-full bg-[var(--yellow2)] shadow-md">
	<div class="mx-auto px-20 sm:px-20 lg:px-20">
		<div class="flex h-20 items-center justify-between">
			<!-- Logo -->
			<div class="flex-shrink-0 text-xl font-bold text-[var(--grey1)]">
				<a class="flex-direction-column align-center flex" href="/"
					><img class="h-16 w-16" src="LukaSilniLogo.png" alt="" />
					<h1 class="text-center">Kod Luke Silnog</h1></a
				>
			</div>

			<!-- Desktop links -->
			<div class="hidden space-x-8 text-[var(--grey1)] lg:flex">
				<a href="/meni" class="">Meni</a>
				<a href="/o-nama" class="">O nama</a>
				<a href="/galerija" class="">Galerija</a>
				<a href="/lokacija" class="">Lokacija</a>
				<a href="/kontakt" class="">Kontakt</a>
			</div>

			<!-- Mobile menu button -->
			<div class="lg:hidden">
				<button on:click={() => (isOpen = !isOpen)} class="text-[var(--grey1)] focus:outline-none">
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
		<div class="space-y-2 bg-[var(--yellow3)] px-4 pt-2 pb-4 shadow-md lg:hidden">
			<a href="/meni" class="block text-[var(--grey1)]">Meni</a>
			<a href="/o-nama" class="block text-[var(--grey1)]">O nama</a>
			<a href="/galerija" class="block text-[var(--grey1)]">Galerija</a>
			<a href="/lokacija" class="block text-[var(--grey1)]">Lokacija</a>
			<a href="/kontakt" class="block text-[var(--grey1)]">Kontakt</a>
		</div>
	{/if}
</nav>

<style>
</style>
