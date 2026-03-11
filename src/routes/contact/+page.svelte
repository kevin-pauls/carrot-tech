<script lang="ts">
	let form = $state({ name: '', email: '', company: '', message: '', subject: 'demo' });
	let status = $state<'idle' | 'loading' | 'success' | 'error'>('idle');
	let errors = $state<Record<string, string>>({});

	function validate() {
		errors = {};
		if (!form.name.trim()) errors.name = 'Name is required.';
		if (!form.email.trim() || !form.email.includes('@')) errors.email = 'Valid email required.';
		if (!form.message.trim()) errors.message = 'Message is required.';
		return Object.keys(errors).length === 0;
	}

	async function handleSubmit(e: SubmitEvent) {
		e.preventDefault();
		if (!validate()) return;
		status = 'loading';
		await new Promise((r) => setTimeout(r, 1000));
		status = 'success';
	}
</script>

<svelte:head>
	<title>Contact — Carrot</title>
	<meta name="description" content="Get in touch with the Carrot team. Book a demo, ask a question or find our offices in Oslo and Bergen." />
</svelte:head>

<section class="hero">
	<div class="container">
		<span class="hero-label">Contact</span>
		<h1>Let's talk circular<br /><em>economy.</em></h1>
		<p class="hero-sub">Whether you're ready to book a demo, have a question about our products, or just want to learn more — we'd love to hear from you.</p>
	</div>
</section>

<hr class="section-divider" />

<section class="contact-main">
	<div class="container contact-inner">
		<!-- Contact Info -->
		<div class="contact-info">
			<div class="info-block">
				<h2>Get in touch</h2>
				<p>Our team typically responds within one business day.</p>

				<div class="contact-methods">
					<a href="mailto:hello@carrot.tech" class="contact-method">
						<div class="method-icon">
							<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
								<path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/>
								<polyline points="22,6 12,13 2,6"/>
							</svg>
						</div>
						<div>
							<div class="method-label">Email</div>
							<div class="method-value">hello@carrot.tech</div>
						</div>
					</a>
					<button class="contact-method" onclick={() => {}}>
						<div class="method-icon orange">
							<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
								<rect x="3" y="4" width="18" height="18" rx="2" ry="2"/>
								<line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/>
								<line x1="3" y1="10" x2="21" y2="10"/>
							</svg>
						</div>
						<div>
							<div class="method-label">Book a meeting</div>
							<div class="method-value">30-min discovery call</div>
						</div>
					</button>
				</div>
			</div>

			<div class="divider"></div>

			<!-- Offices -->
			<div class="offices">
				<h3>Our offices</h3>
				<div class="office-grid">
					<div class="office-card">
						<div class="office-city">Oslo</div>
						<address>
							Nedre Slottsgate 5<br />
							0157 Oslo<br />
							Norway
						</address>
					</div>
					<div class="office-card">
						<div class="office-city">Bergen</div>
						<address>
							Vestre Strømkaien 7<br />
							5008 Bergen<br />
							Norway
						</address>
					</div>
				</div>
			</div>

			<div class="divider"></div>

			<!-- Company info -->
			<div class="company-block">
				<h3>Company details</h3>
				<dl>
					<dt>Legal name</dt>
					<dd>Carrot AS</dd>
					<dt>Org. number</dt>
					<dd>920 018 734</dd>
					<dt>Incorporated</dt>
					<dd>Bergen, Norway, 2017</dd>
				</dl>
			</div>
		</div>

		<!-- Contact Form -->
		<div class="form-panel">
			{#if status === 'success'}
				<div class="success-panel">
					<div class="success-icon">
						<svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
							<polyline points="20 6 9 17 4 12"></polyline>
						</svg>
					</div>
					<h2>Message sent!</h2>
					<p>Thanks for reaching out. We'll get back to you within one business day.</p>
					<button class="btn btn-outline" onclick={() => { status = 'idle'; form = { name: '', email: '', company: '', message: '', subject: 'demo' }; }}>
						Send another message
					</button>
				</div>
			{:else}
				<form onsubmit={handleSubmit} class="contact-form" novalidate>
					<h2>Send us a message</h2>

					<div class="form-row">
						<div class="form-group" class:has-error={!!errors.name}>
							<label for="name">Full name <span class="required">*</span></label>
							<input id="name" type="text" bind:value={form.name} placeholder="Your name" disabled={status === 'loading'} />
							{#if errors.name}<span class="field-error">{errors.name}</span>{/if}
						</div>
						<div class="form-group" class:has-error={!!errors.email}>
							<label for="email">Work email <span class="required">*</span></label>
							<input id="email" type="email" bind:value={form.email} placeholder="you@company.com" disabled={status === 'loading'} />
							{#if errors.email}<span class="field-error">{errors.email}</span>{/if}
						</div>
					</div>

					<div class="form-row">
						<div class="form-group">
							<label for="company">Company</label>
							<input id="company" type="text" bind:value={form.company} placeholder="Your company" disabled={status === 'loading'} />
						</div>
						<div class="form-group">
							<label for="subject">I'm interested in</label>
							<select id="subject" bind:value={form.subject} disabled={status === 'loading'}>
								<option value="demo">Booking a demo</option>
								<option value="real-estate">Commercial Real Estate</option>
								<option value="municipal">Municipal Waste Management</option>
								<option value="partnership">Partnership</option>
								<option value="other">Something else</option>
							</select>
						</div>
					</div>

					<div class="form-group full" class:has-error={!!errors.message}>
						<label for="message">Message <span class="required">*</span></label>
						<textarea id="message" bind:value={form.message} placeholder="Tell us about your project or question..." rows="5" disabled={status === 'loading'}></textarea>
						{#if errors.message}<span class="field-error">{errors.message}</span>{/if}
					</div>

					<button type="submit" class="btn btn-black submit-btn" disabled={status === 'loading'}>
						{#if status === 'loading'}
							<span class="spinner"></span> Sending...
						{:else}
							Send message
							<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
								<line x1="22" y1="2" x2="11" y2="13"></line>
								<polygon points="22 2 15 22 11 13 2 9 22 2"></polygon>
							</svg>
						{/if}
					</button>
				</form>
			{/if}
		</div>
	</div>
</section>

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

	h1 em { font-style: italic; }

	.hero-sub {
		font-size: 18px;
		line-height: 1.6;
		max-width: 540px;
		opacity: 0.75;
	}

	/* Contact main */
	.contact-main {
		padding: 80px 0;
	}

	.contact-inner {
		display: grid;
		grid-template-columns: 360px 1fr;
		gap: 80px;
		align-items: start;
	}

	.info-block h2 {
		font-family: var(--font-display);
		font-size: 28px;
		font-weight: 700;
		letter-spacing: -0.01em;
		margin-bottom: 8px;
	}

	.info-block > p {
		font-size: 15px;
		color: var(--gray-5);
		margin-bottom: 24px;
	}

	.contact-methods {
		display: flex;
		flex-direction: column;
		gap: 8px;
	}

	.contact-method {
		display: flex;
		align-items: center;
		gap: 16px;
		padding: 16px;
		border: 1.5px solid var(--black);
		clip-path: var(--clip-corner-lg);
		text-decoration: none;
		color: var(--black);
		background: var(--white);
		cursor: pointer;
		font-family: var(--font-primary);
		width: 100%;
		text-align: left;
		transition: background 0.15s ease;
	}

	.contact-method:hover {
		background: var(--gray-1);
	}

	.method-icon {
		width: 44px;
		height: 44px;
		background: var(--lime);
		clip-path: var(--clip-corner);
		display: flex;
		align-items: center;
		justify-content: center;
		flex-shrink: 0;
	}

	.method-icon.orange {
		background: var(--orange);
	}

	.method-label {
		font-size: 12px;
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 0.06em;
		color: var(--gray-5);
		margin-bottom: 2px;
	}

	.method-value {
		font-size: 15px;
		font-weight: 600;
	}

	.divider {
		border-top: 1px solid var(--gray-2);
		margin: 32px 0;
	}

	.offices h3, .company-block h3 {
		font-size: 14px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		color: var(--gray-5);
		margin-bottom: 16px;
	}

	.office-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 16px;
	}

	.office-card {
		padding: 16px;
		background: var(--gray-1);
		clip-path: var(--clip-corner);
	}

	.office-city {
		font-size: 15px;
		font-weight: 700;
		margin-bottom: 8px;
	}

	.office-card address {
		font-style: normal;
		font-size: 13px;
		line-height: 1.7;
		color: var(--gray-6);
	}

	.company-block dl {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 6px 16px;
	}

	.company-block dt {
		font-size: 12px;
		font-weight: 600;
		color: var(--gray-5);
		text-transform: uppercase;
		letter-spacing: 0.06em;
	}

	.company-block dd {
		font-size: 14px;
		font-weight: 500;
	}

	/* Form */
	.form-panel {
		background: var(--white);
		border: 1.5px solid var(--black);
		clip-path: var(--clip-corner-lg);
		padding: 48px;
	}

	.contact-form h2 {
		font-family: var(--font-display);
		font-size: 28px;
		font-weight: 700;
		letter-spacing: -0.01em;
		margin-bottom: 32px;
	}

	.form-row {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 16px;
		margin-bottom: 16px;
	}

	.form-group {
		display: flex;
		flex-direction: column;
		gap: 6px;
	}

	.form-group.full {
		margin-bottom: 24px;
	}

	label {
		font-size: 13px;
		font-weight: 600;
	}

	.required {
		color: #e53e3e;
	}

	input, select, textarea {
		padding: 12px 16px;
		font-size: 15px;
		border: 1.5px solid var(--gray-3);
		background: var(--white);
		clip-path: var(--clip-corner);
		outline: none;
		transition: border-color 0.15s ease;
		font-family: var(--font-primary);
		color: var(--black);
	}

	input:focus, select:focus, textarea:focus {
		border-color: var(--black);
	}

	.has-error input,
	.has-error textarea {
		border-color: #e53e3e;
	}

	.field-error {
		font-size: 12px;
		color: #c53030;
	}

	textarea {
		resize: vertical;
		min-height: 120px;
	}

	select {
		appearance: none;
		background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='14' height='14' viewBox='0 0 24 24' fill='none' stroke='%236f6c6c' stroke-width='2'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");
		background-repeat: no-repeat;
		background-position: right 14px center;
		padding-right: 40px;
	}

	.submit-btn {
		width: 100%;
		justify-content: center;
		padding: 16px;
		font-size: 16px;
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

	/* Success */
	.success-panel {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		gap: 16px;
		padding: 40px 0;
	}

	.success-icon {
		width: 72px;
		height: 72px;
		background: var(--lime);
		clip-path: var(--clip-corner-lg);
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.success-panel h2 {
		font-family: var(--font-display);
		font-size: 28px;
		font-weight: 700;
	}

	.success-panel p {
		font-size: 16px;
		color: var(--gray-6);
		max-width: 360px;
	}

	/* Responsive */
	@media (max-width: 1100px) {
		.contact-inner {
			grid-template-columns: 1fr;
			gap: 48px;
		}
	}

	@media (max-width: 560px) {
		.form-panel {
			padding: 28px 20px;
		}

		.form-row {
			grid-template-columns: 1fr;
		}
	}
</style>
