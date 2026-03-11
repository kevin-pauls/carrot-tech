<script lang="ts">
	interface Stat {
		value: string;
		label: string;
	}
	interface Props {
		label?: string;
		title: string;
		description: string;
		stats: Stat[];
		imageSrc?: string;
		imageAlt?: string;
		ctaText?: string;
		ctaHref?: string;
		accent?: 'lime' | 'orange' | 'beige';
	}

	let {
		label = 'Case Study',
		title,
		description,
		stats,
		imageSrc,
		imageAlt = 'Case study image',
		ctaText = 'Read case study',
		ctaHref = '#',
		accent = 'lime'
	}: Props = $props();
</script>

<section class="case-study" data-accent={accent}>
	<div class="container inner">
		<div class="cs-image">
			<img
				src={imageSrc ?? `https://placehold.co/640x480/E7EB5D/000000?text=${encodeURIComponent(title)}`}
				alt={imageAlt}
				loading="lazy"
			/>
		</div>
		<div class="cs-content">
			<span class="cs-label">{label}</span>
			<h2>{title}</h2>
			<p>{description}</p>

			<div class="cs-stats">
				{#each stats as stat}
					<div class="cs-stat">
						<div class="stat-value">{stat.value}</div>
						<div class="stat-label">{stat.label}</div>
					</div>
				{/each}
			</div>

			{#if ctaHref && ctaText}
				<a href={ctaHref} class="btn btn-black">
					{ctaText}
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
						<line x1="5" y1="12" x2="19" y2="12"></line>
						<polyline points="12 5 19 12 12 19"></polyline>
					</svg>
				</a>
			{/if}
		</div>
	</div>
</section>

<style>
	.case-study {
		border-top: 1px solid var(--black);
		padding: 0;
	}

	.case-study[data-accent='lime'] {
		background: var(--lime);
	}
	.case-study[data-accent='orange'] {
		background: var(--orange);
	}
	.case-study[data-accent='beige'] {
		background: var(--beige);
	}

	.inner {
		display: grid;
		grid-template-columns: 1fr 1fr;
		min-height: 480px;
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
		padding: 64px 56px;
		display: flex;
		flex-direction: column;
		gap: 20px;
	}

	.cs-label {
		font-size: 12px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		opacity: 0.6;
	}

	h2 {
		font-family: var(--font-display);
		font-size: clamp(26px, 3vw, 38px);
		font-weight: 700;
		letter-spacing: -0.01em;
		line-height: 1.2;
	}

	p {
		font-size: 16px;
		line-height: 1.6;
		opacity: 0.85;
		max-width: 480px;
	}

	.cs-stats {
		display: flex;
		gap: 32px;
		flex-wrap: wrap;
		margin-top: 8px;
	}

	.cs-stat {
		display: flex;
		flex-direction: column;
		gap: 4px;
	}

	.stat-value {
		font-size: 36px;
		font-weight: 800;
		letter-spacing: -0.03em;
		line-height: 1;
	}

	.stat-label {
		font-size: 13px;
		opacity: 0.65;
		font-weight: 500;
	}

	@media (max-width: 735px) {
		.inner {
			grid-template-columns: 1fr;
		}

		.cs-image {
			border-right: none;
			border-bottom: 1px solid var(--black);
			height: 260px;
		}

		.cs-content {
			padding: 40px 24px;
		}
	}
</style>
