<script lang="ts">
</script>

<footer>
	<div class="container">
		<div class="footer-grid">
			<div class="footer-col">
				<div class="footer-logo">
					<svg width="110" height="28" viewBox="0 0 110 28" fill="none" xmlns="http://www.w3.org/2000/svg">
						<rect width="28" height="28" fill="#FF8736" style="clip-path: polygon(4px 0%, calc(100% - 4px) 0%, 100% 4px, 100% calc(100% - 4px), calc(100% - 4px) 100%, 4px 100%, 0% calc(100% - 4px), 0% 4px);" />
						<text x="14" y="20" text-anchor="middle" font-family="DM Sans, sans-serif" font-weight="700" font-size="14" fill="white">C</text>
						<text x="42" y="20" font-family="DM Sans, sans-serif" font-weight="700" font-size="18" fill="white">carrot</text>
					</svg>
				</div>
				<p class="footer-tagline">Closing the circularity gap by rewarding sustainable behaviour.</p>
			</div>

			<div class="footer-col">
				<h3 class="footer-heading">Product</h3>
				<ul class="footer-links">
					<li><a href="/product/real-estate">Commercial Real Estate</a></li>
					<li><a href="/product/municipal-waste-management">Municipal Waste Management</a></li>
					<li><a href="/product/real-estate#tenants">Carrot for Tenants</a></li>
					<li><a href="/product/real-estate#api">The Carrot API</a></li>
				</ul>
			</div>

			<div class="footer-col">
				<h3 class="footer-heading">Company</h3>
				<ul class="footer-links">
					<li><a href="/why-carrot">Our why</a></li>
					<li><a href="/about">About us</a></li>
					<li><a href="/about#careers">Careers</a></li>
					<li><a href="/contact">Contact</a></li>
					<li><a href="/articles/vestkanten-shopping-mall">Case Studies</a></li>
				</ul>
			</div>

			<div class="footer-col">
				<h3 class="footer-heading">Follow us</h3>
				<ul class="footer-links social-links">
					<li>
						<a href="https://linkedin.com/company/carrot-tech" target="_blank" rel="noopener noreferrer">
							<svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
							LinkedIn
						</a>
					</li>
					<li>
						<a href="https://twitter.com/carrottech" target="_blank" rel="noopener noreferrer">
							<svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"/></svg>
							Twitter / X
						</a>
					</li>
					<li>
						<a href="https://instagram.com/carrottechnology" target="_blank" rel="noopener noreferrer">
							<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
							Instagram
						</a>
					</li>
				</ul>
			</div>

			<div class="footer-col company-info">
				<h3 class="footer-heading">Carrot AS</h3>
				<address>
					<p>Org.nr: 920 018 734</p>
					<p>Nedre Slottsgate 5</p>
					<p>0157 Oslo, Norway</p>
					<p class="mt-8">
						<a href="mailto:hello@carrot.tech">hello@carrot.tech</a>
					</p>
				</address>
			</div>
		</div>

		<div class="footer-bottom">
			<p>&copy; {new Date().getFullYear()} Carrot AS. All rights reserved.</p>
			<div class="footer-bottom-links">
				<a href="/privacy">Privacy Policy</a>
				<a href="/terms">Terms of Service</a>
			</div>
		</div>
	</div>
</footer>

<style>
	footer {
		background: var(--black);
		color: var(--white);
		padding: 64px 0 32px;
		border-top: 1px solid var(--black);
	}

	.footer-grid {
		display: grid;
		grid-template-columns: 1.5fr 1fr 1fr 1fr 1.5fr;
		gap: 48px;
		padding-bottom: 48px;
		border-bottom: 1px solid rgba(255, 255, 255, 0.15);
		margin-bottom: 32px;
	}

	.footer-logo {
		margin-bottom: 16px;
	}

	.footer-tagline {
		font-size: 14px;
		color: rgba(255, 255, 255, 0.6);
		line-height: 1.6;
		max-width: 220px;
	}

	.footer-heading {
		font-size: 12px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		color: rgba(255, 255, 255, 0.5);
		margin-bottom: 16px;
	}

	.footer-links {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 10px;
	}

	.footer-links a {
		font-size: 14px;
		color: rgba(255, 255, 255, 0.75);
		transition: color 0.15s ease;
		text-decoration: none;
	}

	.footer-links a:hover {
		color: var(--lime);
	}

	.social-links a {
		display: flex;
		align-items: center;
		gap: 8px;
	}

	.company-info address {
		font-style: normal;
	}

	.company-info address p {
		font-size: 14px;
		color: rgba(255, 255, 255, 0.75);
		line-height: 1.7;
	}

	.company-info address a {
		color: var(--lime);
		text-decoration: none;
		font-size: 14px;
	}

	.company-info address a:hover {
		text-decoration: underline;
	}

	.mt-8 {
		margin-top: 8px;
	}

	.footer-bottom {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 16px;
	}

	.footer-bottom p {
		font-size: 13px;
		color: rgba(255, 255, 255, 0.4);
	}

	.footer-bottom-links {
		display: flex;
		gap: 24px;
	}

	.footer-bottom-links a {
		font-size: 13px;
		color: rgba(255, 255, 255, 0.4);
		text-decoration: none;
		transition: color 0.15s ease;
	}

	.footer-bottom-links a:hover {
		color: rgba(255, 255, 255, 0.7);
	}

	@media (max-width: 1100px) {
		.footer-grid {
			grid-template-columns: 1fr 1fr 1fr;
		}
	}

	@media (max-width: 735px) {
		.footer-grid {
			grid-template-columns: 1fr 1fr;
			gap: 32px;
		}

		.footer-col:first-child {
			grid-column: 1 / -1;
		}

		.footer-bottom {
			flex-direction: column;
			align-items: flex-start;
			gap: 12px;
		}
	}

	@media (max-width: 560px) {
		.footer-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
