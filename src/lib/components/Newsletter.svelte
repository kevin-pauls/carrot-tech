<script lang="ts">
	let email = $state('');
	let status = $state<'idle' | 'loading' | 'success' | 'error'>('idle');
	let errorMsg = $state('');

	async function handleSubmit(e: SubmitEvent) {
		e.preventDefault();
		if (!email || !email.includes('@')) {
			errorMsg = 'Please enter a valid email address.';
			return;
		}
		status = 'loading';
		errorMsg = '';
		// Simulate API call
		await new Promise((r) => setTimeout(r, 800));
		status = 'success';
		email = '';
	}
</script>

<section class="newsletter">
	<div class="container inner">
		<div class="newsletter-content">
			<h2>Stay in the loop</h2>
			<p>Get insights on circular economy, waste management and sustainability — delivered to your inbox.</p>
		</div>

		{#if status === 'success'}
			<div class="success-msg">
				<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
					<polyline points="20 6 9 17 4 12"></polyline>
				</svg>
				Thanks! You're on the list.
			</div>
		{:else}
			<form onsubmit={handleSubmit} class="newsletter-form" novalidate>
				<div class="input-wrap">
					<input
						type="email"
						placeholder="Enter your email"
						bind:value={email}
						aria-label="Email address"
						class:error={!!errorMsg}
						disabled={status === 'loading'}
					/>
					<button type="submit" class="btn btn-black" disabled={status === 'loading'}>
						{#if status === 'loading'}
							<span class="spinner"></span>
						{:else}
							Subscribe
						{/if}
					</button>
				</div>
				{#if errorMsg}
					<p class="error-msg">{errorMsg}</p>
				{/if}
			</form>
		{/if}
	</div>
</section>

<style>
	.newsletter {
		background: var(--lime);
		border-top: 1px solid var(--black);
		border-bottom: 1px solid var(--black);
		padding: 48px 0;
	}

	.inner {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 40px;
	}

	.newsletter-content h2 {
		font-size: 26px;
		font-weight: 700;
		margin-bottom: 8px;
		letter-spacing: -0.01em;
	}

	.newsletter-content p {
		font-size: 15px;
		color: var(--seaweed);
		max-width: 400px;
	}

	.newsletter-form {
		flex-shrink: 0;
	}

	.input-wrap {
		display: flex;
		gap: 8px;
	}

	input {
		padding: 12px 18px;
		font-size: 15px;
		border: 1.5px solid var(--black);
		background: var(--white);
		width: 280px;
		clip-path: var(--clip-corner);
		outline: none;
		transition: border-color 0.15s ease;
	}

	input:focus {
		border-color: var(--black);
		box-shadow: 0 0 0 3px rgba(0,0,0,0.1);
	}

	input.error {
		border-color: #e53e3e;
	}

	.error-msg {
		color: #c53030;
		font-size: 13px;
		margin-top: 6px;
	}

	.success-msg {
		display: flex;
		align-items: center;
		gap: 8px;
		font-size: 16px;
		font-weight: 600;
		color: var(--seaweed);
		padding: 12px 20px;
		background: rgba(0,0,0,0.06);
		clip-path: var(--clip-corner);
	}

	.spinner {
		width: 16px;
		height: 16px;
		border: 2px solid rgba(255,255,255,0.3);
		border-top-color: white;
		border-radius: 50%;
		animation: spin 0.7s linear infinite;
		display: inline-block;
	}

	@keyframes spin {
		to { transform: rotate(360deg); }
	}

	@media (max-width: 735px) {
		.inner {
			flex-direction: column;
			align-items: flex-start;
		}

		.newsletter-form {
			width: 100%;
		}

		.input-wrap {
			flex-direction: column;
		}

		input {
			width: 100%;
		}

		.btn {
			width: 100%;
			justify-content: center;
		}
	}
</style>
