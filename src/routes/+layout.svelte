<script>
	import { page } from '$app/stores';
	import '../app.css';
</script>

<main class="overscroll-none min-h-screen -mb-12">
	<slot />
</main>

<footer class="sticky bottom-0 h-12">
	<nav data-sveltekit-prefetch>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg>
		<ul>
			<li class:active={$page.url.pathname === '/' && ($page.url.hash == ''||$page.url.hash == '#home')}>
				<a href="/#home">Home</a>
			</li>
			<li class:active={$page.url.hash === '#roadmap'}>
				<a href="/#roadmap">Roadmap</a>
			</li>
			<li class:active={$page.url.hash === '#goals'}>
				<a href="/#goals">Goals</a>
			</li>
			<li class:active={$page.url.hash === '#more'}>
				<a href="/#more">More</a>
			</li>
		</ul>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg>
	</nav>
</footer>

<style>
	footer {
		/* display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px; */

		display: flex;
		justify-content: center;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
		@apply origin-center rotate-180;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}
</style>
