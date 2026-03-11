<script lang="ts">
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	let mobileOpen = $state(false);
	let productDropdownOpen = $state(false);
	let scrolled = $state(false);

	onMount(() => {
		const handleScroll = () => {
			scrolled = window.scrollY > 10;
		};
		window.addEventListener('scroll', handleScroll, { passive: true });
		return () => window.removeEventListener('scroll', handleScroll);
	});

	function toggleMobile() {
		mobileOpen = !mobileOpen;
		if (mobileOpen) document.body.style.overflow = 'hidden';
		else document.body.style.overflow = '';
	}

	function closeMobile() {
		mobileOpen = false;
		document.body.style.overflow = '';
	}
</script>

<header class:scrolled>
	<div class="container inner">
		<a href="/" class="logo" onclick={closeMobile}>
			<svg width="110" height="28" viewBox="0 0 110 28" fill="none" xmlns="http://www.w3.org/2000/svg">
				<rect width="28" height="28" rx="0" fill="#FF8736" style="clip-path: polygon(4px 0%, calc(100% - 4px) 0%, 100% 4px, 100% calc(100% - 4px), calc(100% - 4px) 100%, 4px 100%, 0% calc(100% - 4px), 0% 4px);" />
				<text x="14" y="20" text-anchor="middle" font-family="DM Sans, sans-serif" font-weight="700" font-size="14" fill="white">C</text>
				<text x="42" y="20" font-family="DM Sans, sans-serif" font-weight="700" font-size="18" fill="currentColor">carrot</text>
			</svg>
		</a>

		<nav class="desktop-nav">
			<div
				class="nav-item dropdown"
				role="navigation"
				onmouseenter={() => (productDropdownOpen = true)}
				onmouseleave={() => (productDropdownOpen = false)}
			>
				<button class="nav-link" aria-expanded={productDropdownOpen}>
					Product
					<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
						<polyline points="6 9 12 15 18 9"></polyline>
					</svg>
				</button>
				{#if productDropdownOpen}
					<div class="dropdown-menu">
						<a href="/product/real-estate" class="dropdown-item">
							<span class="dropdown-icon">
								<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
							</span>
							<div>
								<div class="dropdown-title">Commercial Real Estate</div>
								<div class="dropdown-desc">Waste management for properties</div>
							</div>
						</a>
						<a href="/product/municipal-waste-management" class="dropdown-item">
							<span class="dropdown-icon">
								<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M3 3h18v4H3z"/><path d="M5 7v14h14V7"/><path d="M10 11v6"/><path d="M14 11v6"/></svg>
							</span>
							<div>
								<div class="dropdown-title">Municipal Waste Management</div>
								<div class="dropdown-desc">Smart solutions for municipalities</div>
							</div>
						</a>
					</div>
				{/if}
			</div>
			<a href="/why-carrot" class="nav-link" class:active={$page.url.pathname === '/why-carrot'}>Our why</a>
			<a href="/about" class="nav-link" class:active={$page.url.pathname === '/about'}>About us</a>
			<a href="/contact" class="nav-link" class:active={$page.url.pathname === '/contact'}>Contact</a>
		</nav>

		<div class="header-actions">
			<a href="/contact" class="btn btn-black">Demo</a>
			<a href="#login" class="nav-link login-link">Log in</a>
		</div>

		<button class="hamburger" onclick={toggleMobile} aria-label="Toggle menu" aria-expanded={mobileOpen}>
			{#if mobileOpen}
				<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
					<line x1="18" y1="6" x2="6" y2="18"></line>
					<line x1="6" y1="6" x2="18" y2="18"></line>
				</svg>
			{:else}
				<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
					<line x1="3" y1="6" x2="21" y2="6"></line>
					<line x1="3" y1="12" x2="21" y2="12"></line>
					<line x1="3" y1="18" x2="21" y2="18"></line>
				</svg>
			{/if}
		</button>
	</div>
</header>

{#if mobileOpen}
	<div class="mobile-overlay" role="button" tabindex="0" aria-label="Close menu" onclick={closeMobile} onkeydown={(e) => e.key === 'Enter' && closeMobile()}></div>
	<nav class="mobile-nav">
		<a href="/" class="mobile-nav-link" onclick={closeMobile}>Home</a>
		<div class="mobile-section-label">Product</div>
		<a href="/product/real-estate" class="mobile-nav-link indent" onclick={closeMobile}>Commercial Real Estate</a>
		<a href="/product/municipal-waste-management" class="mobile-nav-link indent" onclick={closeMobile}>Municipal Waste Management</a>
		<a href="/why-carrot" class="mobile-nav-link" onclick={closeMobile}>Our why</a>
		<a href="/about" class="mobile-nav-link" onclick={closeMobile}>About us</a>
		<a href="/contact" class="mobile-nav-link" onclick={closeMobile}>Contact</a>
		<div class="mobile-actions">
			<a href="/contact" class="btn btn-black" onclick={closeMobile}>Book Demo</a>
			<a href="#login" class="btn btn-outline" onclick={closeMobile}>Log in</a>
		</div>
	</nav>
{/if}

<style>
	header {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		height: var(--header-height);
		background: var(--white);
		border-bottom: 1px solid var(--black);
		z-index: 100;
		transition: box-shadow 0.2s ease;
	}

	header.scrolled {
		box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
	}

	.inner {
		display: flex;
		align-items: center;
		height: 100%;
		gap: 24px;
	}

	.logo {
		flex-shrink: 0;
		color: var(--black);
	}

	.desktop-nav {
		display: flex;
		align-items: center;
		gap: 4px;
		flex: 1;
		justify-content: center;
	}

	.nav-item {
		position: relative;
	}

	.nav-link {
		display: inline-flex;
		align-items: center;
		gap: 4px;
		padding: 8px 14px;
		font-size: 15px;
		font-weight: 500;
		color: var(--black);
		background: none;
		border: none;
		cursor: pointer;
		border-radius: 4px;
		transition: background 0.15s ease;
		text-decoration: none;
	}

	.nav-link:hover,
	.nav-link.active {
		background: var(--gray-2);
	}

	.dropdown-menu {
		position: absolute;
		top: calc(100% + 8px);
		left: 50%;
		transform: translateX(-50%);
		background: var(--white);
		border: 1px solid var(--black);
		min-width: 280px;
		clip-path: var(--clip-corner-lg);
		padding: 8px;
		z-index: 200;
	}

	.dropdown-item {
		display: flex;
		align-items: flex-start;
		gap: 12px;
		padding: 12px;
		border-radius: 4px;
		transition: background 0.15s ease;
		text-decoration: none;
		color: var(--black);
	}

	.dropdown-item:hover {
		background: var(--gray-1);
	}

	.dropdown-icon {
		width: 36px;
		height: 36px;
		background: var(--lime);
		display: flex;
		align-items: center;
		justify-content: center;
		clip-path: var(--clip-corner);
		flex-shrink: 0;
		margin-top: 2px;
	}

	.dropdown-title {
		font-size: 14px;
		font-weight: 600;
		margin-bottom: 2px;
	}

	.dropdown-desc {
		font-size: 12px;
		color: var(--gray-6);
	}

	.header-actions {
		display: flex;
		align-items: center;
		gap: 8px;
		flex-shrink: 0;
	}

	.login-link {
		padding: 8px 14px;
	}

	.hamburger {
		display: none;
		padding: 8px;
		cursor: pointer;
		background: none;
		border: none;
		color: var(--black);
	}

	.mobile-overlay {
		position: fixed;
		inset: 0;
		background: rgba(0, 0, 0, 0.4);
		z-index: 98;
		top: var(--header-height);
	}

	.mobile-nav {
		position: fixed;
		top: var(--header-height);
		left: 0;
		right: 0;
		background: var(--white);
		border-bottom: 1px solid var(--black);
		padding: 16px 24px 24px;
		z-index: 99;
		display: flex;
		flex-direction: column;
		gap: 4px;
	}

	.mobile-nav-link {
		display: block;
		padding: 12px 16px;
		font-size: 16px;
		font-weight: 500;
		color: var(--black);
		border-radius: 4px;
		transition: background 0.15s ease;
	}

	.mobile-nav-link:hover {
		background: var(--gray-2);
	}

	.mobile-nav-link.indent {
		padding-left: 32px;
		font-size: 15px;
		font-weight: 400;
		color: var(--gray-6);
	}

	.mobile-section-label {
		padding: 12px 16px 4px;
		font-size: 12px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		color: var(--gray-5);
	}

	.mobile-actions {
		display: flex;
		flex-direction: column;
		gap: 8px;
		margin-top: 16px;
		padding-top: 16px;
		border-top: 1px solid var(--gray-2);
	}

	.mobile-actions .btn {
		text-align: center;
		justify-content: center;
	}

	@media (max-width: 735px) {
		.desktop-nav {
			display: none;
		}

		.header-actions {
			display: none;
		}

		.hamburger {
			display: flex;
			margin-left: auto;
		}
	}
</style>
