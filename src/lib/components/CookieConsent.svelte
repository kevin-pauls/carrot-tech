<script lang="ts">
	import { onMount } from 'svelte';

	let visible = $state(false);

	onMount(() => {
		const consent = localStorage.getItem('carrot-cookie-consent');
		if (!consent) {
			setTimeout(() => (visible = true), 1500);
		}
	});

	function accept() {
		localStorage.setItem('carrot-cookie-consent', 'accepted');
		visible = false;
	}

	function decline() {
		localStorage.setItem('carrot-cookie-consent', 'declined');
		visible = false;
	}
</script>

{#if visible}
	<div class="cookie-banner" role="dialog" aria-label="Cookie consent">
		<div class="cookie-content">
			<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
				<path d="M12 2a10 10 0 1 0 10 10c0-.55-.05-1.1-.14-1.63a3 3 0 0 1-3.23-3.23A3 3 0 0 1 15 4.14 10 10 0 0 0 12 2z"/>
				<path d="M8 14s1.5 2 4 2 4-2 4-2"/>
				<line x1="9" y1="9" x2="9.01" y2="9"/>
				<line x1="15" y1="9" x2="15.01" y2="9"/>
			</svg>
			<p>
				We use cookies to improve your experience. By using our site you agree to our
				<a href="/privacy">privacy policy</a>.
			</p>
		</div>
		<div class="cookie-actions">
			<button class="btn btn-outline btn-sm" onclick={decline}>Decline</button>
			<button class="btn btn-black btn-sm" onclick={accept}>Accept</button>
		</div>
	</div>
{/if}

<style>
	.cookie-banner {
		position: fixed;
		bottom: 24px;
		left: 50%;
		transform: translateX(-50%);
		background: var(--white);
		border: 1.5px solid var(--black);
		clip-path: var(--clip-corner-lg);
		padding: 16px 20px;
		display: flex;
		align-items: center;
		gap: 20px;
		z-index: 1000;
		max-width: 600px;
		width: calc(100% - 48px);
		box-shadow: 0 8px 32px rgba(0,0,0,0.12);
		animation: slideUp 0.3s ease;
	}

	@keyframes slideUp {
		from { transform: translateX(-50%) translateY(20px); opacity: 0; }
		to { transform: translateX(-50%) translateY(0); opacity: 1; }
	}

	.cookie-content {
		display: flex;
		align-items: flex-start;
		gap: 12px;
		flex: 1;
	}

	.cookie-content svg {
		flex-shrink: 0;
		margin-top: 2px;
		color: var(--orange);
	}

	.cookie-content p {
		font-size: 13px;
		line-height: 1.5;
		color: var(--gray-6);
	}

	.cookie-content a {
		color: var(--black);
		text-decoration: underline;
	}

	.cookie-actions {
		display: flex;
		gap: 8px;
		flex-shrink: 0;
	}

	.btn-sm {
		padding: 8px 16px;
		font-size: 13px;
	}

	@media (max-width: 560px) {
		.cookie-banner {
			flex-direction: column;
			align-items: stretch;
		}

		.cookie-actions {
			justify-content: flex-end;
		}
	}
</style>
