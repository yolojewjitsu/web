<script>
	let y = 0; // scroll position

	let homeSection, 
		roadmapSection, 
		goalsSection, 
		moreSection;
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="DGN DAO Web" />
</svelte:head>

<svelte:window bind:scrollY={y}/>

<div class="overscroll-none fixed top-0 right-0">{y}</div>

<div class="overscroll-none snap-y">
    <section 
		bind:this={homeSection}
		id="home" 
		class="pt-4 bg-black snap-start step text-center">
        <!-- Attention -->
        <img src="/logo.svg" height="64px" weight="64px" style="height: 96px; margin: auto;" />
	<h1 style="font-weight: bold; font-size: 2em;">DGN DAO</h1>

	<h3 style="margin-bottom: 1.5em;">
		<strong>ideas grow in value here</strong><br/>
	</h3>
    </section>
    <section
		bind:this={roadmapSection}
		id="roadmap" 
		class="bg-viridis-12 snap-start step">
        <!-- Interest -->
        <h3>Our Journey so far:</h3>
    </section>
    <section
		bind:this={goalsSection}
		id="goals" 
		class="bg-viridis-10 snap-start step">
        <!-- Decision: why we doing what we doing, and who we invite -->
		<h3>What and why we going to do, and who we invite:</h3>
    </section>
    <section 
		bind:this={moreSection}
		id="more" 
		class="pb-12 bg-viridis-8 snap-start step">
        <!-- Action: communication happened, timme to conclude -->
        <h4><strong>Dive deeper: Docs, Whitepaper, Github</strong></h4>
        <h4><strong>Read us: Blog, Twitter</strong></h4>
	    <h4><strong>Online action: Discord, Telegram</strong></h4>
        <h4><strong>Stay in touch: Subscribe to mail list</strong></h4>
	    <h4><strong>Invest: Token, Future token auctions.</strong></h4>
    </section>
</div>

<style>
    .step {
        @apply h-[66vh] bg-transparent;
    }
</style>