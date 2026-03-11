<script lang="ts">
	import FeatureCard from '$lib/components/FeatureCard.svelte';
	import ClientLogos from '$lib/components/ClientLogos.svelte';
	import CaseStudy from '$lib/components/CaseStudy.svelte';
	import CTA from '$lib/components/CTA.svelte';
</script>

<svelte:head>
	<title>Carrot — Closing the circularity gap</title>
	<meta name="description" content="Carrot rewards sustainable behaviour in waste management for commercial real estate and municipalities. Close the circularity gap with data-driven insights." />
</svelte:head>

<!-- Hero -->
<section class="hero">
	<div class="container hero-inner">
		<div class="hero-content">
			<div class="hero-badge">
				<span class="badge-dot"></span>
				Circular economy platform
			</div>
			<h1>Closing the<br />circularity gap by<br /><em>rewarding sustainable</em><br />behaviour.</h1>
			<p class="hero-body">
				Carrot empowers tenants, municipalities and waste operators with the data and incentives they need to sort better, waste less and build a circular economy.
			</p>
			<div class="hero-actions">
				<a href="/contact" class="btn btn-black">Book a demo</a>
				<a href="/why-carrot" class="btn btn-outline">Our why</a>
			</div>
			<div class="hero-trust">
				<span>Trusted by</span>
				<div class="trust-logos">
					{#each ['Entra', 'Statsbygg', 'BIR', 'Ferd'] as name}
						<span class="trust-logo">{name}</span>
					{/each}
				</div>
			</div>
		</div>
		<div class="hero-visual">
			<div class="dot-pattern"></div>
			<div class="hero-morph-wrap">
				<object type="image/svg+xml" data="/hero-animation.svg" class="morph-svg" aria-label="Animated morphing shapes illustrating waste management concepts"></object>
			</div>
		</div>
	</div>
</section>

<!-- Feature Cards -->
<section class="features">
	<div class="container">
		<div class="features-grid">
			<FeatureCard
				title="Flexible data collection"
				description="Integrate with existing waste infrastructure or deploy IoT sensors. Carrot adapts to your setup, not the other way around."
				icon="recycle"
				accent="lime"
			/>
			<FeatureCard
				title="Data-driven improvements"
				description="Powerful dashboards turn raw sorting data into actionable insights — identify issues before they become costly."
				icon="chart"
				accent="orange"
			/>
			<FeatureCard
				title="Empowered tenants"
				description="Give residents and tenants real-time feedback on their sorting behaviour. Motivation through transparency drives lasting change."
				icon="users"
				accent="beige"
			/>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Product: Commercial Real Estate -->
<section class="product-section">
	<div class="container product-inner">
		<div class="product-content">
			<span class="section-label">Product</span>
			<h2>Built for<br /><em>Commercial Real Estate</em></h2>
			<p>
				From single buildings to entire portfolios, Carrot gives property managers the infrastructure, data and tenant engagement tools to dramatically improve waste sorting rates — and prove ESG impact.
			</p>
			<ul class="product-list">
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Real-time sorting data across all fractions
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Tenant-facing app with gamification
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					ESG reporting and certification support
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Open API for property management integration
				</li>
			</ul>
			<a href="/product/real-estate" class="btn btn-black">
				Explore Real Estate
				<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
					<line x1="5" y1="12" x2="19" y2="12"></line>
					<polyline points="12 5 19 12 12 19"></polyline>
				</svg>
			</a>
		</div>
		<div class="product-image">
			<img
				src="https://placehold.co/640x520/E9D7C9/000000?text=Real+Estate+Dashboard"
				alt="Carrot for Commercial Real Estate"
				loading="lazy"
			/>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Product: Municipal Waste Management -->
<section class="product-section reverse">
	<div class="container product-inner">
		<div class="product-image">
			<img
				src="https://placehold.co/640x520/E7EB5D/000000?text=Municipal+Waste+Platform"
				alt="Carrot for Municipal Waste Management"
				loading="lazy"
			/>
		</div>
		<div class="product-content">
			<span class="section-label">Product</span>
			<h2>Smarter<br /><em>Municipal Waste Management</em></h2>
			<p>
				Help municipalities motivate households to sort better. Carrot's Pay-As-You-Throw model, statistics dashboards and household engagement tools create measurable, lasting change.
			</p>
			<ul class="product-list">
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Vendor-lock-in free open platform
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Pay-As-You-Throw waste fee model
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Household statistics and gamification
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Seamless integration with existing waste operators
				</li>
			</ul>
			<a href="/product/municipal-waste-management" class="btn btn-black">
				Explore Municipal
				<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
					<line x1="5" y1="12" x2="19" y2="12"></line>
					<polyline points="12 5 19 12 12 19"></polyline>
				</svg>
			</a>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- How it works -->
<section class="how-it-works">
	<div class="container">
		<div class="section-header">
			<span class="section-label">How it works</span>
			<h2>The Carrot ecosystem</h2>
			<p>Four interconnected products that cover the full waste management journey — from data collection to behaviour change.</p>
		</div>
		<div class="hiw-grid">
			<div class="hiw-card">
				<div class="hiw-number">01</div>
				<div class="hiw-icon">
					<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
						<rect x="3" y="3" width="18" height="18" rx="2"/><line x1="3" y1="9" x2="21" y2="9"/><line x1="3" y1="15" x2="21" y2="15"/><line x1="9" y1="9" x2="9" y2="21"/><line x1="15" y1="9" x2="15" y2="21"/>
					</svg>
				</div>
				<h3>Carrot Insight</h3>
				<p>The intelligence layer. Real-time dashboards, fraction-level analytics and ESG reports for property managers and municipalities.</p>
			</div>
			<div class="hiw-card">
				<div class="hiw-number">02</div>
				<div class="hiw-icon">
					<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
						<path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/>
					</svg>
				</div>
				<h3>Carrot for Tenants</h3>
				<p>A mobile experience that shows tenants and households their own waste data, rewards good sorting and drives behavioural change.</p>
			</div>
			<div class="hiw-card">
				<div class="hiw-number">03</div>
				<div class="hiw-icon">
					<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
						<path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"/><rect x="8" y="2" width="8" height="4" rx="1" ry="1"/>
					</svg>
				</div>
				<h3>Registration Suite</h3>
				<p>Flexible data collection — from IoT bin sensors to manual registration tools — that integrates with any existing waste infrastructure.</p>
			</div>
			<div class="hiw-card">
				<div class="hiw-number">04</div>
				<div class="hiw-icon">
					<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
						<polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/>
					</svg>
				</div>
				<h3>The Carrot API</h3>
				<p>An open, well-documented API that lets property systems, ERP platforms and third-party apps connect to Carrot's data layer.</p>
			</div>
		</div>
	</div>
</section>

<!-- Client Logos -->
<ClientLogos title="Trusted by leading organisations" />

<hr class="section-divider" />

<!-- Case Study -->
<CaseStudy
	label="Case Study"
	title="Vestkanten Shopping Mall"
	description="Bergen's flagship shopping centre transformed its waste operations with Carrot — achieving a 72% sorting rate and dramatically reducing residual waste sent to incineration."
	stats={[
		{ value: '54%→72%', label: 'Sorting rate improvement' },
		{ value: '80%', label: 'Residual waste reduction' },
		{ value: '110', label: 'Shops onboarded' }
	]}
	ctaText="Read case study"
	ctaHref="/articles/vestkanten-shopping-mall"
	accent="lime"
/>

<hr class="section-divider" />

<!-- Benefits Grid -->
<section class="benefits">
	<div class="container">
		<div class="section-header">
			<span class="section-label">Why Carrot</span>
			<h2>Built for measurable impact</h2>
		</div>
		<div class="benefits-grid">
			<div class="benefit-card">
				<div class="benefit-icon orange">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
						<polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/>
					</svg>
				</div>
				<h3>Proven results</h3>
				<p>Customers see an average 18-percentage-point improvement in sorting rates within the first year.</p>
			</div>
			<div class="benefit-card">
				<div class="benefit-icon lime">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
						<polyline points="1 4 1 10 7 10"/><polyline points="23 20 23 14 17 14"/>
						<path d="M20.49 9A9 9 0 0 0 5.64 5.64L1 10m22 4l-4.64 4.36A9 9 0 0 1 3.51 15"/>
					</svg>
				</div>
				<h3>Plug-and-play integration</h3>
				<p>Carrot connects to your existing waste infrastructure. No forklift upgrade required.</p>
			</div>
			<div class="benefit-card">
				<div class="benefit-icon beige">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
						<rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/>
					</svg>
				</div>
				<h3>Vendor-lock-in free</h3>
				<p>Open architecture means you're never trapped. Switch hardware or operators without losing your data.</p>
			</div>
			<div class="benefit-card">
				<div class="benefit-icon black">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
						<path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>
					</svg>
				</div>
				<h3>ESG-ready reporting</h3>
				<p>Export data for GRESB, BREEAM and EU Taxonomy reporting with one click.</p>
			</div>
		</div>
	</div>
</section>

<CTA
	headline="Ready to close the circularity gap?"
	subtext="Join the organisations already using Carrot to build a circular economy."
	primaryText="Book a demo"
	primaryHref="/contact"
	secondaryText="Explore product"
	secondaryHref="/product/real-estate"
	accent="orange"
/>

<style>
	/* Hero */
	.hero {
		background: var(--lime);
		border-bottom: 1px solid var(--black);
		padding: 80px 0 0;
		overflow: hidden;
	}

	.hero-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 60px;
		align-items: flex-end;
		min-height: 580px;
	}

	.hero-content {
		padding-bottom: 80px;
	}

	.hero-badge {
		display: inline-flex;
		align-items: center;
		gap: 8px;
		padding: 6px 14px;
		background: rgba(0,0,0,0.08);
		clip-path: var(--clip-corner);
		font-size: 13px;
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 0.06em;
		margin-bottom: 24px;
	}

	.badge-dot {
		width: 8px;
		height: 8px;
		border-radius: 50%;
		background: var(--orange);
		flex-shrink: 0;
	}

	h1 {
		font-family: var(--font-display);
		font-size: clamp(38px, 5vw, 68px);
		font-weight: 700;
		line-height: 1.1;
		letter-spacing: -0.02em;
		margin-bottom: 24px;
	}

	h1 em {
		font-style: italic;
		color: var(--seaweed);
	}

	.hero-body {
		font-size: 18px;
		line-height: 1.6;
		max-width: 480px;
		margin-bottom: 36px;
		color: rgba(0,0,0,0.75);
	}

	.hero-actions {
		display: flex;
		gap: 12px;
		margin-bottom: 48px;
	}

	.hero-trust {
		display: flex;
		align-items: center;
		gap: 16px;
		flex-wrap: wrap;
	}

	.hero-trust > span {
		font-size: 13px;
		color: var(--seaweed);
		font-weight: 500;
	}

	.trust-logos {
		display: flex;
		gap: 12px;
		flex-wrap: wrap;
	}

	.trust-logo {
		padding: 4px 10px;
		background: rgba(0,0,0,0.1);
		clip-path: var(--clip-corner);
		font-size: 12px;
		font-weight: 700;
	}

	.hero-visual {
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
		overflow: hidden;
	}

	.dot-pattern {
		position: absolute;
		inset: 0;
		background-image: radial-gradient(circle, var(--black) 1.3px, transparent 1.3px);
		background-size: 22px 22px;
		opacity: 0.16;
		z-index: 0;
	}

	.hero-morph-wrap {
		position: relative;
		z-index: 1;
		width: 90%;
		max-width: 520px;
		aspect-ratio: 1;
	}

	.morph-svg {
		width: 100%;
		height: 100%;
	}

	/* Features */
	.features {
		background: var(--gray-1);
		padding: 64px 0;
		border-bottom: 1px solid var(--black);
	}

	.features-grid {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 20px;
	}

	/* Product Sections */
	.product-section {
		padding: 80px 0;
	}

	.product-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 80px;
		align-items: center;
	}

	.product-section.reverse .product-inner {
		direction: rtl;
	}

	.product-section.reverse .product-content {
		direction: ltr;
	}

	.product-section.reverse .product-image {
		direction: ltr;
	}

	.section-label {
		display: inline-block;
		font-size: 12px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		color: var(--gray-5);
		margin-bottom: 12px;
	}

	.product-content h2 {
		font-family: var(--font-display);
		font-size: clamp(28px, 3.5vw, 44px);
		font-weight: 700;
		letter-spacing: -0.02em;
		line-height: 1.15;
		margin-bottom: 20px;
	}

	.product-content h2 em {
		font-style: italic;
		color: var(--seaweed);
	}

	.product-content > p {
		font-size: 16px;
		line-height: 1.7;
		color: var(--gray-6);
		margin-bottom: 24px;
	}

	.product-list {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 10px;
		margin-bottom: 32px;
	}

	.product-list li {
		display: flex;
		align-items: center;
		gap: 10px;
		font-size: 15px;
		font-weight: 500;
	}

	.product-list li svg {
		flex-shrink: 0;
		color: var(--orange);
	}

	.product-image {
		overflow: hidden;
		clip-path: var(--clip-corner-lg);
		border: 1px solid var(--black);
	}

	.product-image img {
		width: 100%;
		aspect-ratio: 4/3;
		object-fit: cover;
		transition: transform 0.4s ease;
	}

	.product-image:hover img {
		transform: scale(1.03);
	}

	/* How it works */
	.how-it-works {
		padding: 80px 0;
		background: var(--black);
		color: var(--white);
		border-top: 1px solid var(--black);
	}

	.section-header {
		max-width: 640px;
		margin: 0 auto 56px;
		text-align: center;
	}

	.how-it-works .section-label {
		color: rgba(255,255,255,0.4);
	}

	.section-header h2 {
		font-family: var(--font-display);
		font-size: clamp(28px, 3.5vw, 44px);
		font-weight: 700;
		letter-spacing: -0.02em;
		margin-bottom: 16px;
	}

	.section-header p {
		font-size: 16px;
		opacity: 0.7;
		line-height: 1.6;
	}

	.hiw-grid {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 1px;
		background: rgba(255,255,255,0.15);
		border: 1px solid rgba(255,255,255,0.15);
		clip-path: var(--clip-corner-lg);
	}

	.hiw-card {
		background: var(--black);
		padding: 36px 28px;
		display: flex;
		flex-direction: column;
		gap: 16px;
	}

	.hiw-number {
		font-size: 12px;
		font-weight: 700;
		opacity: 0.3;
		letter-spacing: 0.06em;
	}

	.hiw-icon {
		width: 48px;
		height: 48px;
		background: rgba(255,255,255,0.08);
		clip-path: var(--clip-corner);
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.hiw-card h3 {
		font-size: 16px;
		font-weight: 700;
	}

	.hiw-card p {
		font-size: 14px;
		line-height: 1.6;
		opacity: 0.65;
	}

	/* Benefits */
	.benefits {
		padding: 80px 0;
	}

	.benefits .section-header {
		text-align: left;
		margin: 0 0 48px;
	}

	.benefits-grid {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 20px;
	}

	.benefit-card {
		padding: 28px;
		border: 1px solid var(--gray-2);
		clip-path: var(--clip-corner-lg);
		display: flex;
		flex-direction: column;
		gap: 14px;
		transition: border-color 0.2s ease, transform 0.2s ease;
	}

	.benefit-card:hover {
		border-color: var(--black);
		transform: translateY(-2px);
	}

	.benefit-icon {
		width: 48px;
		height: 48px;
		clip-path: var(--clip-corner);
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.benefit-icon.orange { background: var(--orange); }
	.benefit-icon.lime { background: var(--lime); }
	.benefit-icon.beige { background: var(--beige); }
	.benefit-icon.black { background: var(--black); color: var(--white); }

	.benefit-card h3 {
		font-size: 17px;
		font-weight: 700;
		letter-spacing: -0.01em;
	}

	.benefit-card p {
		font-size: 14px;
		line-height: 1.6;
		color: var(--gray-6);
	}

	/* Responsive */
	@media (max-width: 1100px) {
		.hiw-grid {
			grid-template-columns: repeat(2, 1fr);
		}

		.benefits-grid {
			grid-template-columns: repeat(2, 1fr);
		}
	}

	@media (max-width: 735px) {
		.hero-inner {
			grid-template-columns: 1fr;
			min-height: auto;
		}

		.hero-visual {
			display: none;
		}

		.hero-content {
			padding-bottom: 48px;
		}

		.features-grid {
			grid-template-columns: 1fr;
		}

		.product-inner {
			grid-template-columns: 1fr;
			gap: 36px;
		}

		.product-section.reverse .product-inner {
			direction: ltr;
		}

		.product-image {
			order: -1;
		}

		.hiw-grid {
			grid-template-columns: 1fr;
		}

		.benefits-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
