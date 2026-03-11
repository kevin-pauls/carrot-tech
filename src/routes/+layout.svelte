<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Newsletter from '$lib/components/Newsletter.svelte';
	import CookieConsent from '$lib/components/CookieConsent.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link
		href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,700;1,9..40,400&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap"
		rel="stylesheet"
	/>
	<meta name="viewport" content="width=device-width, initial-scale=1" />
</svelte:head>

<Header />
<main>
	{@render children()}
</main>
<Newsletter />
<Footer />
<CookieConsent />

<style>
	:global(*) {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}

	:global(:root) {
		--lime: #e7eb5d;
		--orange: #ff8736;
		--black: #000000;
		--white: #ffffff;
		--seaweed: #72723b;
		--beige: #e9d7c9;
		--gray-1: #f8f1f1;
		--gray-2: #e8e8e8;
		--gray-3: #d4d4d4;
		--gray-4: #b0b0b0;
		--gray-5: #8c8c8c;
		--gray-6: #6f6c6c;

		--font-primary: 'DM Sans', system-ui, sans-serif;
		--font-display: 'Playfair Display', Georgia, serif;

		--max-width: 1500px;
		--header-height: 67px;

		--clip-corner: polygon(
			8px 0%,
			calc(100% - 8px) 0%,
			100% 8px,
			100% calc(100% - 8px),
			calc(100% - 8px) 100%,
			8px 100%,
			0% calc(100% - 8px),
			0% 8px
		);
		--clip-corner-lg: polygon(
			16px 0%,
			calc(100% - 16px) 0%,
			100% 16px,
			100% calc(100% - 16px),
			calc(100% - 16px) 100%,
			16px 100%,
			0% calc(100% - 16px),
			0% 16px
		);
	}

	:global(html) {
		font-family: var(--font-primary);
		font-size: 17px;
		line-height: 1.5;
		color: var(--black);
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
	}

	:global(body) {
		overflow-x: hidden;
	}

	:global(a) {
		color: inherit;
		text-decoration: none;
	}

	:global(img) {
		max-width: 100%;
		height: auto;
		display: block;
	}

	:global(button) {
		font-family: var(--font-primary);
		cursor: pointer;
		border: none;
		background: none;
	}

	:global(input, textarea) {
		font-family: var(--font-primary);
	}

	:global(.container) {
		max-width: var(--max-width);
		margin: 0 auto;
		padding: 0 24px;
	}

	:global(.btn) {
		display: inline-flex;
		align-items: center;
		gap: 8px;
		padding: 12px 24px;
		font-size: 15px;
		font-weight: 500;
		clip-path: var(--clip-corner);
		transition: transform 0.15s ease, opacity 0.15s ease;
		cursor: pointer;
	}

	:global(.btn:hover) {
		transform: translateY(-1px);
		opacity: 0.9;
	}

	:global(.btn-black) {
		background: var(--black);
		color: var(--white);
	}

	:global(.btn-lime) {
		background: var(--lime);
		color: var(--black);
	}

	:global(.btn-orange) {
		background: var(--orange);
		color: var(--black);
	}

	:global(.btn-outline) {
		background: transparent;
		color: var(--black);
		border: 1.5px solid var(--black);
		clip-path: var(--clip-corner);
	}

	:global(.btn-white) {
		background: var(--white);
		color: var(--black);
	}

	:global(.section-divider) {
		border: none;
		border-top: 1px solid var(--black);
	}

	:global(.sr-only) {
		position: absolute;
		width: 1px;
		height: 1px;
		padding: 0;
		margin: -1px;
		overflow: hidden;
		clip: rect(0, 0, 0, 0);
		white-space: nowrap;
		border-width: 0;
	}

	main {
		padding-top: var(--header-height);
	}
</style>
