<script lang="ts">
	import FeatureCard from '$lib/components/FeatureCard.svelte';
	import ClientLogos from '$lib/components/ClientLogos.svelte';
	import CaseStudy from '$lib/components/CaseStudy.svelte';
	import CTA from '$lib/components/CTA.svelte';

	const faqs = [
		{
			q: 'Does Carrot require us to replace our existing waste infrastructure?',
			a: 'No. Carrot is designed to work with your existing bins, collection trucks and waste handlers. We connect to existing infrastructure via hardware adapters and APIs, so there\'s no need for a costly "rip and replace" programme.'
		},
		{
			q: 'How does the Pay-As-You-Throw model work?',
			a: 'Carrot tracks the weight and volume of residual (non-recyclable) waste from each household. This data feeds into your fee calculation system, so households that produce less residual waste pay lower fees. This creates a direct financial incentive to sort better.'
		},
		{
			q: 'Is Carrot compatible with our ERP and case management systems?',
			a: 'Yes. Carrot provides a well-documented REST API that allows integration with municipality ERP systems, citizen portals and third-party case management tools. We also offer pre-built integrations for common Nordic municipal software platforms.'
		},
		{
			q: 'What does implementation look like, and how long does it take?',
			a: 'A typical municipal deployment takes 6–12 weeks from contract to go-live, depending on the size of the municipality and the complexity of existing infrastructure. Our customer success team guides you through the entire process.'
		}
	];

	const municipalLogos = [
		{ name: 'BIR', abbr: 'BI' },
		{ name: 'RfD', abbr: 'RF' },
		{ name: 'Renovasjon IKS', abbr: 'RI' },
		{ name: 'Fredrikstad', abbr: 'FK' },
		{ name: 'Bergen', abbr: 'BG' },
		{ name: 'Stavanger', abbr: 'SV' },
	];
</script>

<svelte:head>
	<title>Municipal Waste Management — Carrot</title>
	<meta name="description" content="Motivate waste reduction in your municipality with Pay-As-You-Throw, household engagement and real-time analytics. No vendor lock-in." />
</svelte:head>

<!-- Hero -->
<section class="hero">
	<div class="container hero-inner">
		<div class="hero-content">
			<span class="hero-label">Product — Municipal</span>
			<h1>Motivating<br /><em>waste reduction.</em></h1>
			<p class="hero-body">
				Help your municipality reduce residual waste and increase recycling rates — with a data platform that gives every household a reason to sort better.
			</p>
			<div class="hero-actions">
				<a href="/contact" class="btn btn-black">Book a demo</a>
				<a href="#faq" class="btn btn-outline">Common questions</a>
			</div>
		</div>
		<div class="hero-visual">
			<div class="stat-grid">
				<div class="stat-item big">
					<span class="stat-val">-9%</span>
					<span class="stat-lbl">Residual waste</span>
				</div>
				<div class="stat-item">
					<span class="stat-val">+28%</span>
					<span class="stat-lbl">Plastic recycling</span>
				</div>
				<div class="stat-item">
					<span class="stat-val">Bergen</span>
					<span class="stat-lbl">Pilot municipality</span>
				</div>
				<div class="stat-item">
					<span class="stat-val">6+</span>
					<span class="stat-lbl">Municipalities live</span>
				</div>
			</div>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Feature Cards -->
<section class="features">
	<div class="container">
		<div class="section-header">
			<span class="section-label">Features</span>
			<h2>Built for municipal complexity</h2>
			<p>Carrot's municipal platform addresses the unique challenges of motivating thousands of households spread across an entire municipality.</p>
		</div>
		<div class="features-grid">
			<FeatureCard
				title="Removing Vendor Lock-in"
				description="Carrot's open architecture means you own your data and can switch hardware vendors or waste operators without losing your system."
				icon="lock"
				accent="lime"
				large
			/>
			<FeatureCard
				title="Statistics & Dashboards"
				description="Fraction-level reporting across districts, routes and individual households. Identify hotspots and track improvement over time."
				icon="chart"
				accent="orange"
				large
			/>
			<FeatureCard
				title="Household Dashboard"
				description="Each household gets their own sorting score, historical data and personalised tips — delivered via web portal or app."
				icon="eye"
				accent="beige"
				large
			/>
			<FeatureCard
				title="Pay-As-You-Throw"
				description="Link waste fees directly to sorting behaviour. Households that produce less residual waste pay less — a proven driver of change."
				icon="trending"
				accent="black"
				large
			/>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- How Pay-As-You-Throw works -->
<section class="payt-section">
	<div class="container payt-inner">
		<div class="payt-content">
			<span class="section-label">Pay-As-You-Throw</span>
			<h2>Make sorting make financial sense.</h2>
			<p>
				The most effective way to change household behaviour is to make the financial consequences of waste directly visible. Carrot's Pay-As-You-Throw module does exactly that.
			</p>
			<p>
				Using weight data from smart bins or collection trucks, Carrot calculates each household's residual waste volume and feeds this into your fee system. Households that sort more recyclables — and produce less residual waste — pay less.
			</p>
			<div class="payt-steps">
				<div class="payt-step">
					<div class="step-num">1</div>
					<div>
						<strong>Measure residual waste</strong>
						<p>Smart bins or truck scales capture the weight of each collection, tied to the household address.</p>
					</div>
				</div>
				<div class="payt-step">
					<div class="step-num">2</div>
					<div>
						<strong>Calculate fee</strong>
						<p>Carrot computes each household's monthly waste fee based on their residual waste production.</p>
					</div>
				</div>
				<div class="payt-step">
					<div class="step-num">3</div>
					<div>
						<strong>Show the impact</strong>
						<p>Households see their score, their fee and exactly what they can do to improve — closing the feedback loop.</p>
					</div>
				</div>
			</div>
		</div>
		<div class="payt-image">
			<img
				src="https://placehold.co/520x480/E7EB5D/000000?text=Pay-As-You-Throw"
				alt="Pay-As-You-Throw dashboard"
				loading="lazy"
			/>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Carrot for Households -->
<section class="households-section">
	<div class="container households-inner">
		<div class="households-image">
			<img
				src="https://placehold.co/480x540/E9D7C9/000000?text=Household+App"
				alt="Carrot Household App"
				loading="lazy"
			/>
		</div>
		<div class="households-content">
			<span class="section-label">Citizen experience</span>
			<h2>Carrot for Households</h2>
			<p>
				The household portal gives every citizen a window into their own waste data. Simple, clear feedback that motivates long-term improvement.
			</p>
			<ul class="feature-list">
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Monthly waste report per household
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Fraction-by-fraction breakdown
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Neighbourhood comparisons
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Personalised sorting tips
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Projected waste fee based on current behaviour
				</li>
				<li>
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round">
						<polyline points="20 6 9 17 4 12"></polyline>
					</svg>
					Available via web, iOS and Android
				</li>
			</ul>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- FAQ -->
<section class="faq-section" id="faq">
	<div class="container faq-inner">
		<div class="faq-header">
			<span class="section-label">Common questions</span>
			<h2>Frequently asked questions</h2>
		</div>
		<div class="faq-list">
			{#each faqs as faq}
				<details class="faq-item">
					<summary class="faq-question">
						<span>{faq.q}</span>
						<svg class="faq-icon" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
							<polyline points="6 9 12 15 18 9"></polyline>
						</svg>
					</summary>
					<div class="faq-answer">
						<p>{faq.a}</p>
					</div>
				</details>
			{/each}
		</div>
	</div>
</section>

<!-- Case Study: Bergen -->
<CaseStudy
	label="Case Study"
	title="Bergen Municipality"
	description="Bergen partnered with Carrot to roll out a household waste tracking and feedback programme across 15,000 homes. Within 18 months, residual waste dropped by 9% and plastic recycling increased by 28%."
	stats={[
		{ value: '-9%', label: 'Residual waste' },
		{ value: '+28%', label: 'Plastic recycling' },
		{ value: '15,000', label: 'Households enrolled' }
	]}
	ctaText="Read case study"
	ctaHref="/contact"
	accent="lime"
/>

<!-- Municipal Client Logos -->
<section class="municipal-logos">
	<div class="container">
		<p class="logos-label">Municipal customers</p>
		<div class="logos-grid">
			{#each municipalLogos as logo}
				<div class="logo-item">
					<div class="logo-placeholder">
						<span class="logo-abbr">{logo.abbr}</span>
						<span class="logo-name">{logo.name}</span>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<CTA
	headline="Bring Carrot to your municipality"
	subtext="Book a demo and see how other municipalities have used Carrot to dramatically reduce residual waste."
	primaryText="Book a demo"
	primaryHref="/contact"
	secondaryText="Contact us"
	secondaryHref="/contact"
	accent="orange"
/>

<style>
	/* Hero */
	.hero {
		background: var(--beige);
		padding: 80px 0;
		border-bottom: 1px solid var(--black);
	}

	.hero-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 60px;
		align-items: center;
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
		opacity: 0.8;
		margin-bottom: 32px;
		max-width: 460px;
	}

	.hero-actions {
		display: flex;
		gap: 12px;
	}

	.stat-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 16px;
	}

	.stat-item {
		background: var(--white);
		border: 1px solid var(--black);
		clip-path: var(--clip-corner-lg);
		padding: 24px;
		display: flex;
		flex-direction: column;
		gap: 6px;
	}

	.stat-item.big {
		background: var(--lime);
	}

	.stat-val {
		font-size: 32px;
		font-weight: 800;
		letter-spacing: -0.04em;
		line-height: 1;
	}

	.stat-lbl {
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
		max-width: 640px;
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
		margin-bottom: 12px;
	}

	.section-header p {
		font-size: 16px;
		line-height: 1.6;
		color: var(--gray-6);
	}

	.features-grid {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 20px;
	}

	/* PAYT */
	.payt-section {
		padding: 80px 0;
		background: var(--gray-1);
	}

	.payt-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 80px;
		align-items: center;
	}

	.payt-content h2 {
		font-family: var(--font-display);
		font-size: clamp(26px, 3vw, 38px);
		font-weight: 700;
		letter-spacing: -0.02em;
		margin-bottom: 20px;
	}

	.payt-content > p {
		font-size: 16px;
		line-height: 1.7;
		color: var(--gray-6);
		margin-bottom: 16px;
	}

	.payt-steps {
		display: flex;
		flex-direction: column;
		gap: 16px;
		margin-top: 24px;
	}

	.payt-step {
		display: flex;
		gap: 16px;
		align-items: flex-start;
	}

	.step-num {
		width: 32px;
		height: 32px;
		background: var(--orange);
		clip-path: var(--clip-corner);
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 14px;
		font-weight: 800;
		flex-shrink: 0;
	}

	.payt-step strong {
		display: block;
		font-size: 15px;
		font-weight: 700;
		margin-bottom: 4px;
	}

	.payt-step p {
		font-size: 14px;
		color: var(--gray-6);
		line-height: 1.5;
		margin: 0;
	}

	.payt-image {
		clip-path: var(--clip-corner-lg);
		border: 1px solid var(--black);
		overflow: hidden;
	}

	.payt-image img {
		width: 100%;
		object-fit: cover;
	}

	/* Households */
	.households-section {
		padding: 80px 0;
	}

	.households-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 80px;
		align-items: center;
	}

	.households-image {
		clip-path: var(--clip-corner-lg);
		border: 1px solid var(--black);
		overflow: hidden;
	}

	.households-image img {
		width: 100%;
		object-fit: cover;
	}

	.households-content h2 {
		font-family: var(--font-display);
		font-size: clamp(26px, 3vw, 38px);
		font-weight: 700;
		letter-spacing: -0.02em;
		margin-bottom: 16px;
	}

	.households-content > p {
		font-size: 16px;
		line-height: 1.7;
		color: var(--gray-6);
		margin-bottom: 24px;
	}

	.feature-list {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 10px;
	}

	.feature-list li {
		display: flex;
		align-items: center;
		gap: 10px;
		font-size: 15px;
		font-weight: 500;
	}

	.feature-list li svg {
		flex-shrink: 0;
		color: var(--orange);
	}

	/* FAQ */
	.faq-section {
		padding: 80px 0;
		background: var(--beige);
	}

	.faq-inner {
		display: grid;
		grid-template-columns: 320px 1fr;
		gap: 80px;
		align-items: start;
	}

	.faq-header h2 {
		font-family: var(--font-display);
		font-size: clamp(24px, 2.5vw, 32px);
		font-weight: 700;
		letter-spacing: -0.01em;
	}

	.faq-list {
		display: flex;
		flex-direction: column;
		gap: 0;
	}

	.faq-item {
		border-top: 1px solid rgba(0,0,0,0.15);
	}

	.faq-item:last-child {
		border-bottom: 1px solid rgba(0,0,0,0.15);
	}

	.faq-question {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 16px;
		padding: 20px 0;
		cursor: pointer;
		list-style: none;
		font-size: 16px;
		font-weight: 600;
		line-height: 1.4;
	}

	.faq-question::-webkit-details-marker {
		display: none;
	}

	.faq-icon {
		flex-shrink: 0;
		transition: transform 0.2s ease;
	}

	details[open] .faq-icon {
		transform: rotate(180deg);
	}

	.faq-answer {
		padding-bottom: 20px;
	}

	.faq-answer p {
		font-size: 15px;
		line-height: 1.7;
		color: var(--gray-6);
	}

	/* Municipal logos */
	.municipal-logos {
		padding: 48px 0;
		border-top: 1px solid var(--black);
	}

	.logos-label {
		font-size: 13px;
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		color: var(--gray-5);
		text-align: center;
		margin-bottom: 32px;
	}

	.logos-grid {
		display: grid;
		grid-template-columns: repeat(6, 1fr);
		gap: 16px;
		align-items: center;
	}

	.logo-item {
		display: flex;
		align-items: center;
		justify-content: center;
		filter: grayscale(100%);
		opacity: 0.55;
		transition: opacity 0.2s ease, filter 0.2s ease;
	}

	.logo-item:hover {
		filter: grayscale(0%);
		opacity: 1;
	}

	.logo-placeholder {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 4px;
		padding: 16px 20px;
		border: 1px solid var(--gray-3);
		clip-path: var(--clip-corner);
		width: 100%;
	}

	.logo-abbr {
		font-size: 20px;
		font-weight: 800;
		letter-spacing: -0.02em;
	}

	.logo-name {
		font-size: 10px;
		font-weight: 500;
		text-transform: uppercase;
		letter-spacing: 0.06em;
		color: var(--gray-5);
	}

	/* Responsive */
	@media (max-width: 1100px) {
		.features-grid {
			grid-template-columns: repeat(2, 1fr);
		}
	}

	@media (max-width: 735px) {
		.hero-inner,
		.payt-inner,
		.households-inner {
			grid-template-columns: 1fr;
			gap: 40px;
		}

		.features-grid {
			grid-template-columns: 1fr;
		}

		.faq-inner {
			grid-template-columns: 1fr;
			gap: 32px;
		}

		.logos-grid {
			grid-template-columns: repeat(3, 1fr);
		}
	}
</style>
