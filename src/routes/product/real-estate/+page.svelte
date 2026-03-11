<script lang="ts">
	import FeatureCard from '$lib/components/FeatureCard.svelte';
	import ClientLogos from '$lib/components/ClientLogos.svelte';
	import CaseStudy from '$lib/components/CaseStudy.svelte';
	import CTA from '$lib/components/CTA.svelte';
</script>

<svelte:head>
	<title>Carrot for Real Estate — Waste Intelligence for Property Managers</title>
	<meta name="description" content="Transform waste sorting in your commercial property portfolio with real-time data, tenant engagement and ESG reporting. Trusted by Entra, Statsbygg and more." />
</svelte:head>

<!-- Hero -->
<section class="hero">
	<div class="container hero-inner">
		<div class="hero-content">
			<span class="hero-label">Product — Real Estate</span>
			<h1>Waste intelligence<br /><em>for Real Estate.</em></h1>
			<p class="hero-body">
				Give your property team real-time visibility into waste sorting across every fraction, in every building. Drive behaviour change with tenant engagement, and report ESG impact with confidence.
			</p>
			<div class="hero-actions">
				<a href="/contact" class="btn btn-black">Book a demo</a>
				<a href="/contact" class="btn btn-outline">Talk to sales</a>
			</div>
		</div>
		<div class="hero-image">
			<img
				src="https://placehold.co/640x500/E9D7C9/000000?text=Real+Estate+Platform"
				alt="Carrot Real Estate Dashboard"
			/>
			<div class="hero-stat-card">
				<span class="stat-num">+18pp</span>
				<span class="stat-label">Avg. sorting improvement</span>
			</div>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Feature Cards -->
<section class="features">
	<div class="container">
		<div class="section-header">
			<span class="section-label">Capabilities</span>
			<h2>Everything you need to manage waste at scale</h2>
		</div>
		<div class="features-grid">
			<FeatureCard
				title="Infrastructure"
				description="Connect IoT sensors, smart bins and manual registration tools to get fraction-level data across your entire portfolio."
				icon="wifi"
				accent="lime"
				large
			/>
			<FeatureCard
				title="Tenant engagement"
				description="Motivate tenants with a branded app showing their sorting data, leaderboards and sustainability milestones."
				icon="users"
				accent="orange"
				large
			/>
			<FeatureCard
				title="Actionable insight"
				description="Turn raw data into clear dashboards showing sorting rates, contamination trends and cost drivers — at any scale."
				icon="eye"
				accent="beige"
				large
			/>
			<FeatureCard
				title="Reports & compliance"
				description="Export GRESB, BREEAM and EU Taxonomy reports. Prove ESG impact to investors with certified data."
				icon="clipboard"
				accent="black"
				large
			/>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Case Study 1: West One London -->
<section class="case-study-section">
	<div class="container cs-inner">
		<div class="cs-image">
			<img
				src="https://placehold.co/560x440/B0B0B0/ffffff?text=West+One+London"
				alt="West One Shopping Centre, London"
				loading="lazy"
			/>
		</div>
		<div class="cs-content">
			<span class="cs-label">Case Study</span>
			<h2>West One Shopping<br />Centre, London</h2>
			<p>
				West One deployed Carrot across all retail units and saw dramatic improvements in recycling rates within six months — without changing the bin infrastructure.
			</p>
			<div class="cs-stats">
				<div class="cs-stat">
					<span class="stat-val">+20%</span>
					<span class="stat-lbl">Recycling increase</span>
				</div>
				<div class="cs-stat">
					<span class="stat-val">49.3%→65.9%</span>
					<span class="stat-lbl">Sorting rate</span>
				</div>
			</div>
			<blockquote>
				"Carrot gave us visibility we simply didn't have before. Now we can have data-driven conversations with our tenants about improvement."
				<cite>— Waste Manager, West One Shopping Centre</cite>
			</blockquote>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Capability deep dive -->
<section class="capabilities">
	<div class="container">
		<div class="section-header">
			<span class="section-label">How it works</span>
			<h2>Five pillars of the Carrot Real Estate platform</h2>
		</div>
		<div class="cap-grid">
			<div class="cap-item">
				<div class="cap-num">01</div>
				<div class="cap-icon">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
				</div>
				<h3>Secure data collection</h3>
				<p>Data flows from IoT sensors and manual inputs into Carrot's secure, GDPR-compliant data layer — accessible via dashboard or API.</p>
			</div>
			<div class="cap-item">
				<div class="cap-num">02</div>
				<div class="cap-icon">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="1 4 1 10 7 10"/><polyline points="23 20 23 14 17 14"/><path d="M20.49 9A9 9 0 0 0 5.64 5.64L1 10m22 4l-4.64 4.36A9 9 0 0 1 3.51 15"/></svg>
				</div>
				<h3>Existing infrastructure</h3>
				<p>No rip-and-replace. Carrot integrates with your current bins, compactors and waste handlers via standard APIs and hardware adapters.</p>
			</div>
			<div class="cap-item">
				<div class="cap-num">03</div>
				<div class="cap-icon">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><line x1="18" y1="20" x2="18" y2="10"/><line x1="12" y1="20" x2="12" y2="4"/><line x1="6" y1="20" x2="6" y2="14"/></svg>
				</div>
				<h3>Portfolio analytics</h3>
				<p>Compare performance across buildings, set benchmarks and identify properties with the greatest improvement potential.</p>
			</div>
			<div class="cap-item">
				<div class="cap-num">04</div>
				<div class="cap-icon">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
				</div>
				<h3>Tenant accountability</h3>
				<p>Give each tenant their own dashboard. Make sorting visible, make improvement rewarding, and make conversations data-driven.</p>
			</div>
			<div class="cap-item">
				<div class="cap-num">05</div>
				<div class="cap-icon">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
				</div>
				<h3>Open API</h3>
				<p>Connect Carrot data to your property management system, ERP or BI platform via our well-documented REST API.</p>
			</div>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Carrot for Tenants -->
<section class="tenants-section" id="tenants">
	<div class="container tenants-inner">
		<div class="tenants-content">
			<span class="section-label">Tenant experience</span>
			<h2>Carrot for Tenants</h2>
			<p>
				The tenant-facing app is the behavioural change engine at the heart of Carrot. Tenants see their own sorting data, compare against building averages and receive personalised guidance.
			</p>
			<ul class="tenant-list">
				<li>Real-time sorting score per fraction</li>
				<li>Leaderboards and friendly competition between units</li>
				<li>Push notifications when performance changes</li>
				<li>Tips and guidance on common sorting mistakes</li>
				<li>Milestone celebrations and sustainability badges</li>
			</ul>
		</div>
		<div class="tenants-image">
			<img
				src="https://placehold.co/480x560/E7EB5D/000000?text=Tenant+App"
				alt="Carrot Tenant App"
				loading="lazy"
			/>
		</div>
	</div>
</section>

<!-- Case Study: Vestkanten -->
<CaseStudy
	label="Case Study"
	title="Vestkanten Shopping Mall, Bergen"
	description="Vestkanten used Carrot to connect all 110 shops to a shared waste data platform. The result: sorting rate improved from 54% to 72%, and total residual waste fell from 270,000 to 150,000 kg/year."
	stats={[
		{ value: '270k→150k', label: 'kg residual/year' },
		{ value: '72%', label: 'Sorting rate achieved' },
		{ value: '110', label: 'Shops connected' }
	]}
	ctaText="Read full case study"
	ctaHref="/articles/vestkanten-shopping-mall"
	accent="beige"
/>

<!-- Client Logos -->
<ClientLogos title="Trusted by property leaders" />

<CTA
	headline="Start your waste intelligence journey"
	subtext="Join the growing network of property managers using Carrot to prove ESG impact."
	primaryText="Book a demo"
	primaryHref="/contact"
	secondaryText="Talk to sales"
	secondaryHref="/contact"
	accent="lime"
/>

<style>
	/* Hero */
	.hero {
		background: var(--beige);
		padding: 80px 0 0;
		border-bottom: 1px solid var(--black);
		overflow: hidden;
	}

	.hero-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 60px;
		align-items: flex-end;
	}

	.hero-content {
		padding-bottom: 80px;
	}

	.hero-label {
		display: inline-block;
		font-size: 12px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		opacity: 0.55;
		margin-bottom: 20px;
	}

	h1 {
		font-family: var(--font-display);
		font-size: clamp(36px, 4.5vw, 62px);
		font-weight: 700;
		letter-spacing: -0.02em;
		line-height: 1.1;
		margin-bottom: 24px;
	}

	h1 em { font-style: italic; }

	.hero-body {
		font-size: 17px;
		line-height: 1.7;
		max-width: 460px;
		margin-bottom: 32px;
		opacity: 0.8;
	}

	.hero-actions {
		display: flex;
		gap: 12px;
	}

	.hero-image {
		position: relative;
	}

	.hero-image img {
		width: 100%;
		clip-path: polygon(16px 0%, 100% 0%, 100% 100%, 0% 100%, 0% 16px);
		border-top: 1px solid var(--black);
		border-left: 1px solid var(--black);
	}

	.hero-stat-card {
		position: absolute;
		bottom: 32px;
		left: -20px;
		background: var(--white);
		border: 1.5px solid var(--black);
		clip-path: var(--clip-corner-lg);
		padding: 16px 20px;
		display: flex;
		flex-direction: column;
		box-shadow: 4px 4px 0 var(--black);
	}

	.stat-num {
		font-size: 28px;
		font-weight: 800;
		letter-spacing: -0.03em;
	}

	.stat-label {
		font-size: 12px;
		color: var(--gray-5);
		font-weight: 500;
	}

	/* Features */
	.features {
		padding: 80px 0;
	}

	.section-header {
		margin-bottom: 48px;
	}

	.section-label {
		display: inline-block;
		font-size: 12px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		color: var(--gray-5);
		margin-bottom: 10px;
	}

	.section-header h2 {
		font-family: var(--font-display);
		font-size: clamp(26px, 3vw, 38px);
		font-weight: 700;
		letter-spacing: -0.02em;
	}

	.features-grid {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 20px;
	}

	/* Case Study section (inline, non-component) */
	.case-study-section {
		padding: 0;
	}

	.cs-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		min-height: 460px;
	}

	.cs-image {
		border-right: 1px solid var(--black);
	}

	.cs-image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	.cs-content {
		padding: 56px 48px;
		display: flex;
		flex-direction: column;
		gap: 16px;
		background: var(--gray-1);
	}

	.cs-label {
		font-size: 12px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		color: var(--gray-5);
	}

	.cs-content h2 {
		font-family: var(--font-display);
		font-size: clamp(24px, 2.8vw, 36px);
		font-weight: 700;
		letter-spacing: -0.01em;
	}

	.cs-content > p {
		font-size: 16px;
		line-height: 1.6;
		color: var(--gray-6);
	}

	.cs-stats {
		display: flex;
		gap: 32px;
	}

	.cs-stat {
		display: flex;
		flex-direction: column;
		gap: 4px;
	}

	.stat-val {
		font-size: 30px;
		font-weight: 800;
		letter-spacing: -0.03em;
		line-height: 1;
	}

	.stat-lbl {
		font-size: 12px;
		color: var(--gray-5);
	}

	.cs-content blockquote {
		border-left: 3px solid var(--orange);
		padding: 12px 16px;
		background: var(--white);
		font-style: italic;
		font-size: 15px;
		line-height: 1.6;
		margin: 0;
	}

	.cs-content cite {
		display: block;
		font-style: normal;
		font-size: 12px;
		color: var(--gray-5);
		margin-top: 6px;
	}

	/* Capabilities */
	.capabilities {
		padding: 80px 0;
		background: var(--black);
		color: var(--white);
	}

	.capabilities .section-label {
		color: rgba(255,255,255,0.4);
	}

	.capabilities .section-header h2 {
		color: var(--white);
	}

	.cap-grid {
		display: grid;
		grid-template-columns: repeat(5, 1fr);
		gap: 1px;
		background: rgba(255,255,255,0.1);
		border: 1px solid rgba(255,255,255,0.1);
		clip-path: var(--clip-corner-lg);
	}

	.cap-item {
		background: var(--black);
		padding: 32px 24px;
		display: flex;
		flex-direction: column;
		gap: 12px;
	}

	.cap-num {
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 0.06em;
		opacity: 0.3;
	}

	.cap-icon {
		width: 44px;
		height: 44px;
		background: rgba(255,255,255,0.08);
		clip-path: var(--clip-corner);
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.cap-item h3 {
		font-size: 14px;
		font-weight: 700;
	}

	.cap-item p {
		font-size: 13px;
		line-height: 1.6;
		opacity: 0.6;
	}

	/* Tenants */
	.tenants-section {
		padding: 80px 0;
		background: var(--lime);
		border-top: 1px solid var(--black);
	}

	.tenants-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 80px;
		align-items: center;
	}

	.tenants-content h2 {
		font-family: var(--font-display);
		font-size: clamp(28px, 3vw, 40px);
		font-weight: 700;
		letter-spacing: -0.02em;
		margin-bottom: 16px;
	}

	.tenants-content > p {
		font-size: 16px;
		line-height: 1.7;
		color: var(--seaweed);
		margin-bottom: 24px;
	}

	.tenant-list {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 10px;
	}

	.tenant-list li {
		display: flex;
		align-items: center;
		gap: 10px;
		font-size: 15px;
		font-weight: 500;
	}

	.tenant-list li::before {
		content: '';
		width: 6px;
		height: 6px;
		border-radius: 50%;
		background: var(--black);
		flex-shrink: 0;
	}

	.tenants-image {
		clip-path: var(--clip-corner-lg);
		border: 1px solid var(--black);
		overflow: hidden;
	}

	.tenants-image img {
		width: 100%;
		object-fit: cover;
	}

	/* Responsive */
	@media (max-width: 1200px) {
		.cap-grid {
			grid-template-columns: repeat(3, 1fr);
		}

		.features-grid {
			grid-template-columns: repeat(2, 1fr);
		}
	}

	@media (max-width: 735px) {
		.hero-inner {
			grid-template-columns: 1fr;
		}

		.hero-image {
			display: none;
		}

		.hero-content {
			padding-bottom: 48px;
		}

		.features-grid {
			grid-template-columns: 1fr;
		}

		.cs-inner {
			grid-template-columns: 1fr;
		}

		.cs-image {
			border-right: none;
			border-bottom: 1px solid var(--black);
			height: 240px;
		}

		.cs-content {
			padding: 32px 24px;
		}

		.cap-grid {
			grid-template-columns: 1fr 1fr;
		}

		.tenants-inner {
			grid-template-columns: 1fr;
		}
	}

	@media (max-width: 560px) {
		.cap-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
