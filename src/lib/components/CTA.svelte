<script lang="ts">
	interface Props {
		headline?: string;
		subtext?: string;
		primaryText?: string;
		primaryHref?: string;
		secondaryText?: string;
		secondaryHref?: string;
		accent?: 'lime' | 'orange' | 'beige' | 'black';
	}

	let {
		headline = 'Ready to close the circularity gap?',
		subtext = 'Join leading organisations using Carrot to transform waste management.',
		primaryText = 'Book a demo',
		primaryHref = '/contact',
		secondaryText = 'Learn more',
		secondaryHref = '/why-carrot',
		accent = 'lime'
	}: Props = $props();
</script>

<section class="cta-section" data-accent={accent}>
	<div class="container inner">
		<div class="cta-content">
			<h2>{headline}</h2>
			<p>{subtext}</p>
		</div>
		<div class="cta-actions">
			<a href={primaryHref} class="btn" class:btn-black={accent !== 'black'} class:btn-lime={accent === 'black'}>{primaryText}</a>
			{#if secondaryText}
				<a href={secondaryHref} class="btn btn-outline">{secondaryText}</a>
			{/if}
		</div>
	</div>
</section>

<style>
	.cta-section {
		padding: 80px 0;
		border-top: 1px solid var(--black);
	}

	.cta-section[data-accent='lime'] { background: var(--lime); }
	.cta-section[data-accent='orange'] { background: var(--orange); }
	.cta-section[data-accent='beige'] { background: var(--beige); }
	.cta-section[data-accent='black'] { background: var(--black); color: var(--white); }

	.cta-section[data-accent='black'] .btn-outline {
		border-color: var(--white);
		color: var(--white);
	}

	.inner {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 40px;
	}

	.cta-content h2 {
		font-family: var(--font-display);
		font-size: clamp(26px, 3vw, 40px);
		font-weight: 700;
		letter-spacing: -0.01em;
		margin-bottom: 12px;
	}

	.cta-content p {
		font-size: 16px;
		opacity: 0.8;
		max-width: 460px;
	}

	.cta-actions {
		display: flex;
		gap: 12px;
		flex-shrink: 0;
	}

	@media (max-width: 735px) {
		.inner {
			flex-direction: column;
			align-items: flex-start;
		}

		.cta-actions {
			flex-direction: column;
			width: 100%;
		}

		.btn {
			width: 100%;
			justify-content: center;
			text-align: center;
		}
	}
</style>
