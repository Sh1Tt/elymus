<template>
	<div class="hero min-h-screen bg-base-200">
		<div class="hero-content text-center">
			<div
				class="
					max-w-md
					flex
					justify-center
					flex-col
					items-center
					align-items-center
				"
			>
				<h1 class="text-5xl font-bold">Elymus</h1>
				<p class="py-6">
					While we are living in the year 2022, your content on the internet can be censored!
					Your voice can be blocked, even be removed completely! This is why Elymus is created. 
					Elymus places data availability above all. Censoring Elymus sites is as complex as 
					getting rid of wildgrass in your garden: even if a single seed of grass is left, it 
					will grow and spawn new grass. Same goes for Elymus: If there's a single way to load 
					the website, the site will be loaded and cached, growing it's availability.
				</p>
				<a
					class="btn btn-primary"
					href="/setupSettings
                "
				>
					Get Started
				</a>
			</div>
		</div>
		<ConnectWallet />
	</div>
</template>
<script setup>
const router = useRouter();
if (await elApi.kvGet("setuped")) {
	router.push({ path: "/home" });
}
</script>
