<script lang="ts">
	interface Props {
		title?: string;
	}
	let { title = 'Trusted by industry leaders' }: Props = $props();

	const logos = [
		{ name: 'Avantor', abbr: 'AV' },
		{ name: 'Entra', abbr: 'EN' },
		{ name: 'Statsbygg', abbr: 'SB' },
		{ name: 'Ferd', abbr: 'FD' },
		{ name: 'Aspelin Ramm', abbr: 'AR' },
		{ name: 'Braathen', abbr: 'BR' },
		{ name: 'Thon Eiendom', abbr: 'TE' },
		{ name: 'Obos', abbr: 'OB' },
		{ name: 'NCC', abbr: 'NC' },
		{ name: 'Statkraft', abbr: 'SK' },
		{ name: 'Norconsult', abbr: 'NO' },
		{ name: 'BIR', abbr: 'BI' },
	];
</script>

<section class="client-logos">
	<div class="container">
		<p class="logos-label">{title}</p>
		<div class="logos-grid">
			{#each logos as logo}
				<div class="logo-item" title={logo.name}>
					<div class="logo-placeholder">
						<span class="logo-abbr">{logo.abbr}</span>
						<span class="logo-name">{logo.name}</span>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	.client-logos {
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
		max-width: 140px;
	}

	.logo-abbr {
		font-size: 20px;
		font-weight: 800;
		letter-spacing: -0.02em;
		color: var(--black);
	}

	.logo-name {
		font-size: 10px;
		font-weight: 500;
		text-transform: uppercase;
		letter-spacing: 0.06em;
		color: var(--gray-5);
	}

	@media (max-width: 735px) {
		.logos-grid {
			grid-template-columns: repeat(3, 1fr);
		}
	}

	@media (max-width: 560px) {
		.logos-grid {
			grid-template-columns: repeat(2, 1fr);
		}
	}
</style>
