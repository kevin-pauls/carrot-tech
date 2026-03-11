<script lang="ts">
	import CTA from '$lib/components/CTA.svelte';

	const team = [
		{ name: 'Karoline Vabø', role: 'CEO', initials: 'KV' },
		{ name: 'Eivind Røneid', role: 'CTO', initials: 'ER' },
		{ name: 'Marte Haaland', role: 'CPO', initials: 'MH' },
		{ name: 'Jonas Berg', role: 'Head of Sales', initials: 'JB' },
	];

	const timeline = [
		{ year: '2017', event: 'Founded in Bergen', desc: 'Carrot was born from a collaboration between New & Company and BIR (Bergen municipality waste operator) to tackle poor waste sorting in commercial properties.' },
		{ year: '2018', event: 'First commercial deployment', desc: 'Vestkanten Shopping Mall becomes the first live deployment of the Carrot platform, establishing proof of concept.' },
		{ year: '2020', event: 'Municipal expansion', desc: 'Carrot expands into municipal waste management, launching Pay-As-You-Throw capabilities for Norwegian municipalities.' },
		{ year: '2021', event: 'Norselab backing', desc: 'Norselab, Norway\'s leading impact-focused venture studio, backs Carrot to accelerate growth and European expansion.' },
		{ year: '2023', event: 'International growth', desc: 'Carrot launches its first UK-based deployment and begins expansion across Scandinavia and Northern Europe.' },
		{ year: '2024', event: 'Platform 3.0', desc: 'Launch of the fully rebuilt Carrot platform with open API, advanced analytics and a redesigned tenant experience.' },
	];

	const openPositions = [
		{ title: 'Senior Full-Stack Engineer', location: 'Oslo / Remote', type: 'Full-time' },
		{ title: 'Product Designer', location: 'Bergen / Oslo', type: 'Full-time' },
		{ title: 'Account Executive — UK', location: 'London', type: 'Full-time' },
	];
</script>

<svelte:head>
	<title>About Us — Carrot</title>
	<meta name="description" content="Founded in Bergen in 2017, Carrot is on a mission to close the circularity gap through data and behaviour change. Learn our story." />
</svelte:head>

<!-- Hero -->
<section class="hero">
	<div class="container">
		<span class="hero-label">About us</span>
		<h1>A circular world<br /><em>fueled by data.</em></h1>
		<p class="hero-sub">We're a team of engineers, sustainability practitioners and product thinkers building the tools the circular economy needs.</p>
	</div>
</section>

<hr class="section-divider" />

<!-- Mission -->
<section class="mission">
	<div class="container mission-inner">
		<div class="mission-text">
			<span class="section-label">Our mission</span>
			<h2>We believe data is the most powerful tool for sustainability.</h2>
			<p>
				The circular economy cannot be built on good intentions alone. It requires systems that create visibility, accountability and incentives at scale. That's what Carrot does.
			</p>
			<p>
				We make it possible for property managers to see exactly how well waste is sorted in their buildings. We make it possible for municipalities to motivate households with real feedback. And we make it possible for tenants and residents to understand the impact of their choices.
			</p>
			<p>
				Our mission is simple: close the circularity gap. We do this by building products that make sustainable behaviour the easy, rewarding choice — not the difficult one.
			</p>
		</div>
		<div class="mission-values">
			<div class="value-card">
				<span class="value-num">01</span>
				<h3>Data over assumptions</h3>
				<p>Every feature we build starts with real data. We measure what matters and let evidence guide decisions.</p>
			</div>
			<div class="value-card">
				<span class="value-num">02</span>
				<h3>Open by design</h3>
				<p>We build open systems that integrate with existing infrastructure. No lock-in, no walled gardens.</p>
			</div>
			<div class="value-card">
				<span class="value-num">03</span>
				<h3>Impact at scale</h3>
				<p>We're not interested in marginal gains. We want to change how waste management works systemically.</p>
			</div>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Company History -->
<section class="history">
	<div class="container">
		<div class="history-header">
			<span class="section-label">Our story</span>
			<h2>From Bergen to Europe</h2>
		</div>
		<div class="timeline">
			{#each timeline as item, i}
				<div class="timeline-item" class:right={i % 2 !== 0}>
					<div class="timeline-year">{item.year}</div>
					<div class="timeline-content">
						<h3>{item.event}</h3>
						<p>{item.desc}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Founding context -->
<section class="founding">
	<div class="container founding-inner">
		<div class="founding-image">
			<img
				src="https://placehold.co/560x400/E7EB5D/000000?text=Bergen+Office"
				alt="Carrot's Bergen office"
				loading="lazy"
			/>
		</div>
		<div class="founding-text">
			<span class="section-label">Founding story</span>
			<h2>Born from a real problem,<br />built with real partners.</h2>
			<p>
				Carrot was founded in Bergen, Norway in 2017 as a joint venture between <strong>New &amp; Company</strong>, a Norwegian digital agency, and <strong>BIR</strong>, Bergen municipality's waste management company.
			</p>
			<p>
				The founding insight was simple: BIR could see aggregate waste data but had no visibility into what was happening at the fraction level, across individual buildings or tenants. And tenants had no feedback at all.
			</p>
			<p>
				In 2021, <strong>Norselab</strong> — Norway's leading impact-focused venture builder — backed Carrot to scale the platform and expand into new markets.
			</p>
			<div class="backing-logos">
				<div class="backing-logo">New & Company</div>
				<div class="backing-logo">BIR</div>
				<div class="backing-logo">Norselab</div>
			</div>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Team -->
<section class="team-section">
	<div class="container">
		<div class="team-header">
			<span class="section-label">The team</span>
			<h2>People who care about the problem</h2>
			<p>We're a cross-functional team of engineers, sustainability experts and product thinkers — united by a shared mission.</p>
		</div>
		<div class="team-grid">
			{#each team as member}
				<div class="team-card">
					<div class="team-avatar">
						<span>{member.initials}</span>
					</div>
					<div class="team-info">
						<h3>{member.name}</h3>
						<span>{member.role}</span>
					</div>
				</div>
			{/each}
			<div class="team-card placeholder-card">
				<div class="team-avatar plus">
					<span>+</span>
				</div>
				<div class="team-info">
					<h3>Join the team</h3>
					<span>We're hiring</span>
				</div>
			</div>
		</div>
	</div>
</section>

<hr class="section-divider" />

<!-- Careers -->
<section class="careers" id="careers">
	<div class="container">
		<div class="careers-header">
			<div>
				<span class="section-label">Careers</span>
				<h2>Help us build the circular economy</h2>
				<p>We're a fast-growing team with offices in Oslo and Bergen. We value autonomy, impact and craftsmanship.</p>
			</div>
			<a href="mailto:hello@carrot.tech" class="btn btn-black">Open application</a>
		</div>
		<div class="positions-list">
			{#each openPositions as pos}
				<div class="position-item">
					<div class="position-info">
						<h3>{pos.title}</h3>
						<div class="position-meta">
							<span>
								<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
									<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/>
								</svg>
								{pos.location}
							</span>
							<span>
								<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
									<rect x="2" y="7" width="20" height="14" rx="2" ry="2"/><path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16"/>
								</svg>
								{pos.type}
							</span>
						</div>
					</div>
					<a href="mailto:hello@carrot.tech" class="btn btn-outline">Apply</a>
				</div>
			{/each}
		</div>
	</div>
</section>

<CTA
	headline="Want to work together?"
	subtext="Whether you're a potential customer, partner or future team member — we'd love to hear from you."
	primaryText="Get in touch"
	primaryHref="/contact"
	secondaryText="View product"
	secondaryHref="/product/real-estate"
	accent="lime"
/>

<style>
	/* Hero */
	.hero {
		background: var(--lime);
		padding: 96px 0 80px;
		border-bottom: 1px solid var(--black);
	}

	.hero-label {
		font-size: 13px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		opacity: 0.55;
		margin-bottom: 20px;
		display: block;
	}

	h1 {
		font-family: var(--font-display);
		font-size: clamp(38px, 5vw, 68px);
		font-weight: 700;
		letter-spacing: -0.02em;
		line-height: 1.1;
		margin-bottom: 24px;
	}

	h1 em {
		font-style: italic;
	}

	.hero-sub {
		font-size: 19px;
		line-height: 1.6;
		max-width: 540px;
		opacity: 0.75;
	}

	/* Mission */
	.mission {
		padding: 80px 0;
	}

	.mission-inner {
		display: grid;
		grid-template-columns: 1fr 360px;
		gap: 80px;
		align-items: start;
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

	.mission-text h2 {
		font-family: var(--font-display);
		font-size: clamp(24px, 2.5vw, 34px);
		font-weight: 700;
		letter-spacing: -0.01em;
		line-height: 1.2;
		margin-bottom: 24px;
	}

	.mission-text p {
		font-size: 17px;
		line-height: 1.75;
		color: var(--gray-6);
		margin-bottom: 20px;
	}

	.mission-values {
		display: flex;
		flex-direction: column;
		gap: 16px;
	}

	.value-card {
		padding: 24px;
		border: 1px solid var(--gray-2);
		clip-path: var(--clip-corner-lg);
		transition: border-color 0.2s ease;
	}

	.value-card:hover {
		border-color: var(--black);
	}

	.value-num {
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 0.08em;
		color: var(--gray-4);
		display: block;
		margin-bottom: 8px;
	}

	.value-card h3 {
		font-size: 15px;
		font-weight: 700;
		margin-bottom: 8px;
	}

	.value-card p {
		font-size: 13px;
		line-height: 1.6;
		color: var(--gray-6);
	}

	/* History */
	.history {
		padding: 80px 0;
		background: var(--gray-1);
	}

	.history-header {
		margin-bottom: 56px;
	}

	.history-header h2 {
		font-family: var(--font-display);
		font-size: clamp(28px, 3vw, 40px);
		font-weight: 700;
		letter-spacing: -0.02em;
	}

	.timeline {
		display: flex;
		flex-direction: column;
		gap: 24px;
		position: relative;
	}

	.timeline::before {
		content: '';
		position: absolute;
		left: 100px;
		top: 0;
		bottom: 0;
		width: 1px;
		background: var(--gray-3);
	}

	.timeline-item {
		display: grid;
		grid-template-columns: 100px 1fr;
		gap: 40px;
		align-items: start;
	}

	.timeline-year {
		font-size: 14px;
		font-weight: 800;
		color: var(--orange);
		padding-top: 4px;
		text-align: right;
	}

	.timeline-content {
		background: var(--white);
		border: 1px solid var(--gray-2);
		clip-path: var(--clip-corner-lg);
		padding: 20px 24px;
		transition: border-color 0.2s ease;
	}

	.timeline-content:hover {
		border-color: var(--black);
	}

	.timeline-content h3 {
		font-size: 16px;
		font-weight: 700;
		margin-bottom: 6px;
	}

	.timeline-content p {
		font-size: 14px;
		line-height: 1.6;
		color: var(--gray-6);
	}

	/* Founding */
	.founding {
		padding: 80px 0;
	}

	.founding-inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 80px;
		align-items: center;
	}

	.founding-image {
		clip-path: var(--clip-corner-lg);
		border: 1px solid var(--black);
		overflow: hidden;
	}

	.founding-image img {
		width: 100%;
		aspect-ratio: 4/3;
		object-fit: cover;
	}

	.founding-text h2 {
		font-family: var(--font-display);
		font-size: clamp(24px, 2.5vw, 34px);
		font-weight: 700;
		letter-spacing: -0.01em;
		margin-bottom: 20px;
	}

	.founding-text p {
		font-size: 16px;
		line-height: 1.7;
		color: var(--gray-6);
		margin-bottom: 16px;
	}

	.backing-logos {
		display: flex;
		gap: 12px;
		margin-top: 24px;
		flex-wrap: wrap;
	}

	.backing-logo {
		padding: 8px 16px;
		background: var(--lime);
		clip-path: var(--clip-corner);
		font-size: 13px;
		font-weight: 700;
	}

	/* Team */
	.team-section {
		padding: 80px 0;
		background: var(--gray-1);
	}

	.team-header {
		margin-bottom: 48px;
	}

	.team-header h2 {
		font-family: var(--font-display);
		font-size: clamp(26px, 3vw, 38px);
		font-weight: 700;
		letter-spacing: -0.02em;
		margin-bottom: 12px;
	}

	.team-header p {
		font-size: 16px;
		color: var(--gray-6);
	}

	.team-grid {
		display: grid;
		grid-template-columns: repeat(5, 1fr);
		gap: 16px;
	}

	.team-card {
		background: var(--white);
		border: 1px solid var(--gray-2);
		clip-path: var(--clip-corner-lg);
		padding: 24px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 16px;
		text-align: center;
		transition: border-color 0.2s ease, transform 0.2s ease;
	}

	.team-card:hover {
		border-color: var(--black);
		transform: translateY(-2px);
	}

	.placeholder-card {
		background: var(--lime);
	}

	.team-avatar {
		width: 72px;
		height: 72px;
		background: var(--lime);
		clip-path: var(--clip-corner);
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 20px;
		font-weight: 800;
	}

	.team-avatar.plus {
		background: var(--black);
		color: var(--lime);
		font-size: 28px;
	}

	.team-info h3 {
		font-size: 15px;
		font-weight: 700;
		margin-bottom: 4px;
	}

	.team-info span {
		font-size: 13px;
		color: var(--gray-5);
	}

	/* Careers */
	.careers {
		padding: 80px 0;
		background: var(--beige);
	}

	.careers-header {
		display: flex;
		align-items: flex-end;
		justify-content: space-between;
		gap: 24px;
		margin-bottom: 40px;
	}

	.careers-header h2 {
		font-family: var(--font-display);
		font-size: clamp(26px, 3vw, 38px);
		font-weight: 700;
		letter-spacing: -0.02em;
		margin-bottom: 12px;
	}

	.careers-header p {
		font-size: 16px;
		color: var(--gray-6);
		max-width: 480px;
	}

	.positions-list {
		display: flex;
		flex-direction: column;
		gap: 12px;
	}

	.position-item {
		background: var(--white);
		border: 1px solid var(--black);
		clip-path: var(--clip-corner-lg);
		padding: 20px 24px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 20px;
		transition: background 0.15s ease;
	}

	.position-item:hover {
		background: var(--gray-1);
	}

	.position-info h3 {
		font-size: 16px;
		font-weight: 700;
		margin-bottom: 6px;
	}

	.position-meta {
		display: flex;
		gap: 20px;
	}

	.position-meta span {
		display: flex;
		align-items: center;
		gap: 6px;
		font-size: 13px;
		color: var(--gray-5);
	}

	/* Responsive */
	@media (max-width: 1100px) {
		.team-grid {
			grid-template-columns: repeat(3, 1fr);
		}
	}

	@media (max-width: 735px) {
		.mission-inner {
			grid-template-columns: 1fr;
			gap: 48px;
		}

		.founding-inner {
			grid-template-columns: 1fr;
			gap: 40px;
		}

		.timeline::before {
			display: none;
		}

		.timeline-item {
			grid-template-columns: 1fr;
			gap: 8px;
		}

		.timeline-year {
			text-align: left;
		}

		.team-grid {
			grid-template-columns: repeat(2, 1fr);
		}

		.careers-header {
			flex-direction: column;
			align-items: flex-start;
		}

		.position-item {
			flex-direction: column;
			align-items: flex-start;
		}
	}
</style>
