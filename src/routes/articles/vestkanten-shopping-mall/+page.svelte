<script lang="ts">
	import CTA from '$lib/components/CTA.svelte';
</script>

<svelte:head>
	<title>Case Study: Vestkanten Shopping Mall — Carrot</title>
	<meta name="description" content="How Vestkanten Shopping Mall in Bergen improved its sorting rate from 54% to 72% and reduced residual waste by 80% using Carrot." />
</svelte:head>

<!-- Article Hero -->
<section class="article-hero">
	<div class="container">
		<div class="breadcrumb">
			<a href="/">Home</a>
			<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
				<polyline points="9 18 15 12 9 6"></polyline>
			</svg>
			<a href="/product/real-estate">Real Estate</a>
			<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
				<polyline points="9 18 15 12 9 6"></polyline>
			</svg>
			<span>Case Study</span>
		</div>
		<div class="article-meta">
			<span class="meta-tag">Case Study</span>
			<span class="meta-tag">Commercial Real Estate</span>
			<span class="meta-tag">Norway</span>
		</div>
		<h1>Vestkanten Shopping Mall:<br />from 54% to 72% sorting rate</h1>
		<p class="article-subtitle">
			How Bergen's flagship shopping centre transformed its waste management with Carrot — connecting 110 shops and dramatically reducing residual waste.
		</p>
	</div>
</section>

<!-- Hero Image -->
<div class="hero-image-wrap">
	<img
		src="https://placehold.co/1500x600/E9D7C9/000000?text=Vestkanten+Shopping+Mall+Bergen"
		alt="Vestkanten Shopping Mall, Bergen"
	/>
</div>

<hr class="section-divider" />

<!-- Article Layout -->
<section class="article-layout">
	<div class="container article-inner">
		<!-- Sidebar -->
		<aside class="article-sidebar">
			<div class="sidebar-card">
				<h3>Key results</h3>
				<div class="sidebar-stats">
					<div class="sidebar-stat">
						<span class="ss-value">80%</span>
						<span class="ss-label">Reduction in residual waste sent to incineration</span>
					</div>
					<div class="sidebar-stat">
						<span class="ss-value">110</span>
						<span class="ss-label">Shops connected to the Carrot platform</span>
					</div>
					<div class="sidebar-stat">
						<span class="ss-value">54%→72%</span>
						<span class="ss-label">Sorting rate improvement over 18 months</span>
					</div>
					<div class="sidebar-stat">
						<span class="ss-value">270k→150k</span>
						<span class="ss-label">kg residual waste per year</span>
					</div>
				</div>
			</div>

			<div class="sidebar-card info-card">
				<h3>About Vestkanten</h3>
				<dl>
					<dt>Location</dt>
					<dd>Bergen, Norway</dd>
					<dt>Type</dt>
					<dd>Shopping centre</dd>
					<dt>Tenants</dt>
					<dd>110 shops</dd>
					<dt>Deployed</dt>
					<dd>2018</dd>
					<dt>Platform</dt>
					<dd>Carrot Real Estate</dd>
				</dl>
			</div>

			<div class="sidebar-cta">
				<p>Want similar results?</p>
				<a href="/contact" class="btn btn-black" style="width:100%;justify-content:center;">Book a demo</a>
			</div>
		</aside>

		<!-- Article Body -->
		<article class="article-body">
			<section class="article-section">
				<h2>The Challenge: A growing sorting problem</h2>
				<p>
					Vestkanten Shopping Mall is one of Bergen's largest retail destinations, with over 110 individual shops and a waste management challenge that had grown alongside the mall's success. By 2017, the mall's waste manager faced a familiar problem: a growing volume of waste, an unclear picture of what was being sorted correctly, and tenants who had little visibility into their own sorting performance.
				</p>
				<p>
					The mall was sorting at a rate of approximately 54% — meaning nearly half of all waste was being sent to incineration as residual waste. This represented both an environmental and a financial problem. Residual waste is significantly more expensive to process than properly sorted fractions, and the environmental cost of incineration was at odds with the mall's sustainability commitments.
				</p>
				<blockquote>
					"We knew we had a problem, but we didn't know where to start. We couldn't see which tenants were sorting well and which weren't. Without that data, it was impossible to have meaningful conversations or drive improvement."
					<cite>— Waste Manager, Vestkanten Shopping Mall</cite>
				</blockquote>
			</section>

			<section class="article-section">
				<h2>Reduced Residual Waste</h2>
				<p>
					The primary goal of the Carrot deployment was to reduce the volume of residual waste — materials being sent to incineration that could instead be recycled. Within the first year of deployment, residual waste began to fall measurably as tenants gained visibility into their own data.
				</p>
				<p>
					By 2020, total residual waste had fallen from approximately 270,000 kg/year to 150,000 kg/year — a reduction of more than 80,000 kg annually. This translated directly into cost savings on waste disposal and a significant reduction in carbon emissions from incineration.
				</p>
				<div class="inline-stats">
					<div class="inline-stat">
						<span class="is-value">270,000 kg</span>
						<span class="is-label">Residual waste (before)</span>
					</div>
					<div class="inline-arrow">
						<svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
							<line x1="5" y1="12" x2="19" y2="12"></line>
							<polyline points="12 5 19 12 12 19"></polyline>
						</svg>
					</div>
					<div class="inline-stat highlight">
						<span class="is-value">150,000 kg</span>
						<span class="is-label">Residual waste (after)</span>
					</div>
				</div>
			</section>

			<section class="article-section">
				<h2>Counting Everything</h2>
				<p>
					A key element of Vestkanten's success was moving from estimate-based waste tracking to a data-driven approach that captured every fraction — paper, cardboard, plastic, glass, food waste, and residual — at the individual tenant level.
				</p>
				<p>
					Before Carrot, waste data was aggregated across the entire mall, making it impossible to identify which shops were performing well and which were contaminating otherwise clean fractions. Carrot's registration suite changed that completely.
				</p>
				<p>
					Each time a waste collection was made, data on the fraction type and volume was captured and attributed to the relevant tenant. Over time, this built up a detailed picture of sorting performance that the mall's waste manager could use to identify patterns, intervene with underperforming tenants, and celebrate improvements.
				</p>

				<div class="data-table">
					<div class="table-header">Sorting performance by fraction (2020)</div>
					<div class="table-body">
						{#each [
							{ fraction: 'Cardboard', rate: 89, change: '+12pp' },
							{ fraction: 'Plastic', rate: 78, change: '+24pp' },
							{ fraction: 'Glass', rate: 82, change: '+8pp' },
							{ fraction: 'Food waste', rate: 61, change: '+15pp' },
							{ fraction: 'Paper', rate: 91, change: '+9pp' },
							{ fraction: 'Residual', rate: 28, change: '-26pp' },
						] as row}
							<div class="table-row">
								<span class="table-fraction">{row.fraction}</span>
								<div class="table-bar-wrap">
									<div class="table-bar" style="width:{row.rate}%"></div>
								</div>
								<span class="table-rate">{row.rate}%</span>
								<span class="table-change" class:positive={row.change.startsWith('+')} class:negative={row.change.startsWith('-')}>{row.change}</span>
							</div>
						{/each}
					</div>
				</div>
			</section>

			<section class="article-section">
				<h2>Carrot Connects to Existing Infrastructure</h2>
				<p>
					One of the key concerns for Vestkanten's management team was the potential cost and disruption of deploying a new waste management platform. They had existing bin infrastructure, existing waste collection contracts, and 110 tenants with established habits.
				</p>
				<p>
					Carrot's integration model addressed this directly. Rather than replacing existing bins or requiring new waste collection contracts, Carrot connected to Vestkanten's existing waste infrastructure using hardware adapters and a manual registration workflow for tenants.
				</p>
				<p>
					The deployment was completed in phases over eight weeks. In phase one, the registration system was rolled out to the ten largest shops by waste volume. In phase two, the remaining 100 shops were onboarded over four weeks. By the time the full platform was live, tenants were already seeing their data and beginning to engage with the sorting recommendations.
				</p>
				<blockquote>
					"The onboarding was much smoother than we expected. The Carrot team worked with our waste operator to ensure nothing changed in our collection routines — we just gained a data layer on top of what we already had."
					<cite>— Facility Manager, Vestkanten Shopping Mall</cite>
				</blockquote>
			</section>

			<section class="article-section">
				<h2>Tenant engagement: the behavioural layer</h2>
				<p>
					Data alone doesn't change behaviour. Vestkanten's waste manager worked with the Carrot team to design a tenant engagement programme that combined data transparency with social competition.
				</p>
				<p>
					Each tenant received monthly sorting reports showing their performance against the mall average and their own historical data. The top-performing tenants each quarter were recognised in the mall's internal newsletter. Underperforming tenants received direct outreach from the waste manager, now armed with specific data to guide the conversation.
				</p>
				<p>
					Within 12 months, 85% of tenants had viewed their sorting dashboard at least once. Of those, 73% had made at least one visible change to their sorting behaviour based on their data.
				</p>
			</section>

			<section class="article-section conclusion">
				<h2>Conclusion</h2>
				<p>
					Vestkanten Shopping Mall's experience demonstrates what becomes possible when waste management moves from guesswork to data. By connecting 110 tenants to a shared waste data platform, the mall was able to drive an 18-percentage-point improvement in sorting rate and an 80% reduction in residual waste — without replacing a single bin or changing a single collection contract.
				</p>
				<p>
					The lesson is clear: the bottleneck in commercial waste management is almost never infrastructure. It's visibility, accountability and feedback. Carrot provides all three.
				</p>
			</section>

			<!-- Related -->
			<div class="related-content">
				<h3>Explore related content</h3>
				<div class="related-grid">
					<a href="/product/real-estate" class="related-card">
						<span class="related-tag">Product</span>
						<h4>Carrot for Real Estate</h4>
						<p>See all features of the Carrot commercial real estate platform.</p>
					</a>
					<a href="/contact" class="related-card">
						<span class="related-tag">Get started</span>
						<h4>Book a demo</h4>
						<p>See how Carrot can deliver similar results for your property.</p>
					</a>
				</div>
			</div>
		</article>
	</div>
</section>

<CTA
	headline="Ready to transform your waste management?"
	subtext="See how Carrot can deliver measurable results for your property or portfolio."
	primaryText="Book a demo"
	primaryHref="/contact"
	secondaryText="Explore product"
	secondaryHref="/product/real-estate"
	accent="lime"
/>

<style>
	/* Hero */
	.article-hero {
		background: var(--lime);
		padding: 72px 0 64px;
		border-bottom: 1px solid var(--black);
	}

	.breadcrumb {
		display: flex;
		align-items: center;
		gap: 6px;
		margin-bottom: 20px;
		font-size: 13px;
		color: var(--gray-5);
	}

	.breadcrumb a {
		color: var(--gray-5);
		text-decoration: none;
		transition: color 0.15s ease;
	}

	.breadcrumb a:hover {
		color: var(--black);
	}

	.article-meta {
		display: flex;
		gap: 8px;
		margin-bottom: 24px;
		flex-wrap: wrap;
	}

	.meta-tag {
		padding: 4px 12px;
		background: rgba(0,0,0,0.08);
		clip-path: var(--clip-corner);
		font-size: 12px;
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 0.06em;
	}

	h1 {
		font-family: var(--font-display);
		font-size: clamp(32px, 4.5vw, 58px);
		font-weight: 700;
		letter-spacing: -0.02em;
		line-height: 1.1;
		margin-bottom: 20px;
		max-width: 900px;
	}

	.article-subtitle {
		font-size: 18px;
		line-height: 1.6;
		max-width: 680px;
		opacity: 0.75;
	}

	.hero-image-wrap {
		border-bottom: 1px solid var(--black);
	}

	.hero-image-wrap img {
		width: 100%;
		height: 400px;
		object-fit: cover;
	}

	/* Article Layout */
	.article-layout {
		padding: 64px 0 80px;
	}

	.article-inner {
		display: grid;
		grid-template-columns: 300px 1fr;
		gap: 64px;
		align-items: start;
	}

	/* Sidebar */
	.article-sidebar {
		position: sticky;
		top: 96px;
		display: flex;
		flex-direction: column;
		gap: 20px;
	}

	.sidebar-card {
		background: var(--white);
		border: 1px solid var(--black);
		clip-path: var(--clip-corner-lg);
		padding: 24px;
	}

	.sidebar-card h3 {
		font-size: 13px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		color: var(--gray-5);
		margin-bottom: 20px;
	}

	.sidebar-stats {
		display: flex;
		flex-direction: column;
		gap: 20px;
	}

	.sidebar-stat {
		display: flex;
		flex-direction: column;
		gap: 4px;
		padding-bottom: 20px;
		border-bottom: 1px solid var(--gray-2);
	}

	.sidebar-stat:last-child {
		border-bottom: none;
		padding-bottom: 0;
	}

	.ss-value {
		font-size: 28px;
		font-weight: 800;
		letter-spacing: -0.04em;
		line-height: 1;
	}

	.ss-label {
		font-size: 12px;
		color: var(--gray-5);
		line-height: 1.4;
	}

	.info-card dl {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 8px 12px;
	}

	.info-card dt {
		font-size: 12px;
		font-weight: 600;
		color: var(--gray-5);
		text-transform: uppercase;
		letter-spacing: 0.05em;
	}

	.info-card dd {
		font-size: 13px;
		font-weight: 600;
	}

	.sidebar-cta {
		background: var(--lime);
		clip-path: var(--clip-corner-lg);
		padding: 20px;
		display: flex;
		flex-direction: column;
		gap: 12px;
	}

	.sidebar-cta p {
		font-size: 14px;
		font-weight: 600;
		text-align: center;
	}

	/* Article Body */
	.article-body {
		max-width: 720px;
	}

	.article-section {
		margin-bottom: 56px;
	}

	.article-section h2 {
		font-family: var(--font-display);
		font-size: clamp(22px, 2.5vw, 30px);
		font-weight: 700;
		letter-spacing: -0.01em;
		margin-bottom: 20px;
		line-height: 1.2;
	}

	.article-section p {
		font-size: 17px;
		line-height: 1.8;
		color: var(--gray-6);
		margin-bottom: 20px;
	}

	.article-section p:last-child {
		margin-bottom: 0;
	}

	blockquote {
		border-left: 4px solid var(--orange);
		padding: 20px 24px;
		margin: 32px 0;
		background: var(--gray-1);
	}

	blockquote {
		font-family: var(--font-display);
		font-style: italic;
		font-size: 17px;
		line-height: 1.6;
		color: var(--black);
	}

	cite {
		display: block;
		font-style: normal;
		font-family: var(--font-primary);
		font-size: 13px;
		color: var(--gray-5);
		margin-top: 10px;
	}

	/* Inline Stats */
	.inline-stats {
		display: flex;
		align-items: center;
		gap: 24px;
		padding: 28px;
		background: var(--gray-1);
		clip-path: var(--clip-corner-lg);
		margin: 28px 0;
		flex-wrap: wrap;
	}

	.inline-stat {
		display: flex;
		flex-direction: column;
		gap: 4px;
	}

	.inline-stat.highlight {
		background: var(--lime);
		padding: 12px 16px;
		clip-path: var(--clip-corner);
	}

	.is-value {
		font-size: 22px;
		font-weight: 800;
		letter-spacing: -0.03em;
	}

	.is-label {
		font-size: 12px;
		color: var(--gray-5);
	}

	.inline-arrow {
		color: var(--gray-4);
	}

	/* Data Table */
	.data-table {
		margin: 28px 0;
		border: 1px solid var(--gray-2);
		clip-path: var(--clip-corner-lg);
		overflow: hidden;
	}

	.table-header {
		background: var(--gray-2);
		padding: 12px 20px;
		font-size: 13px;
		font-weight: 700;
		letter-spacing: 0.04em;
	}

	.table-row {
		display: grid;
		grid-template-columns: 120px 1fr 50px 60px;
		align-items: center;
		gap: 12px;
		padding: 10px 20px;
		border-top: 1px solid var(--gray-2);
	}

	.table-fraction {
		font-size: 14px;
		font-weight: 500;
	}

	.table-bar-wrap {
		height: 8px;
		background: var(--gray-2);
		clip-path: var(--clip-corner);
		overflow: hidden;
	}

	.table-bar {
		height: 100%;
		background: var(--lime);
		transition: width 0.5s ease;
	}

	.table-rate {
		font-size: 13px;
		font-weight: 700;
		text-align: right;
	}

	.table-change {
		font-size: 12px;
		font-weight: 700;
		text-align: right;
	}

	.table-change.positive { color: #22c55e; }
	.table-change.negative { color: #ef4444; }

	/* Conclusion */
	.conclusion {
		background: var(--lime);
		clip-path: var(--clip-corner-lg);
		padding: 32px;
	}

	.conclusion h2 {
		margin-bottom: 16px;
	}

	.conclusion p {
		color: var(--seaweed);
	}

	/* Related */
	.related-content {
		margin-top: 56px;
		padding-top: 40px;
		border-top: 1px solid var(--gray-2);
	}

	.related-content h3 {
		font-size: 14px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		color: var(--gray-5);
		margin-bottom: 20px;
	}

	.related-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 16px;
	}

	.related-card {
		display: block;
		padding: 24px;
		border: 1px solid var(--gray-2);
		clip-path: var(--clip-corner-lg);
		text-decoration: none;
		color: var(--black);
		transition: border-color 0.15s ease, transform 0.15s ease;
	}

	.related-card:hover {
		border-color: var(--black);
		transform: translateY(-2px);
	}

	.related-tag {
		font-size: 11px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		color: var(--gray-5);
		display: block;
		margin-bottom: 8px;
	}

	.related-card h4 {
		font-size: 16px;
		font-weight: 700;
		margin-bottom: 6px;
	}

	.related-card p {
		font-size: 13px;
		line-height: 1.5;
		color: var(--gray-6);
	}

	/* Responsive */
	@media (max-width: 1000px) {
		.article-inner {
			grid-template-columns: 1fr;
		}

		.article-sidebar {
			position: static;
			display: grid;
			grid-template-columns: 1fr 1fr;
		}
	}

	@media (max-width: 735px) {
		.article-sidebar {
			grid-template-columns: 1fr;
		}

		.table-row {
			grid-template-columns: 100px 1fr 45px 50px;
			gap: 8px;
			padding: 10px 12px;
		}

		.related-grid {
			grid-template-columns: 1fr;
		}

		.inline-stats {
			flex-direction: column;
			align-items: flex-start;
		}
	}
</style>
