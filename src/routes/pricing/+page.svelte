<script>
	import PricingCard from './PricingCard.svelte';

	let tiers = [
		{
			name: 'Basic',
			price: '10',
			features: ['Feature 1', 'Feature 2', 'Feature 3'],
			icon: '/path/to/icon1.png'
		},
		{
			name: 'Pro',
			price: '20',
			features: ['Feature 1', 'Feature 2', 'Feature 3', 'Feature 4'],
			icon: '/path/to/icon2.png'
		},
		{
			name: 'Ultimate',
			price: '30',
			features: ['Feature 1', 'Feature 2', 'Feature 3', 'Feature 4'],
			icon: '/path/to/icon3.png'
		}
	];
</script>

<div class="pricing-container">
	{#each tiers as tier (tier.name)}
		<PricingCard {tier} />
	{/each}
</div>

<style>
	.pricing-container {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 20px;
		padding: 20px;
		background: linear-gradient(to right, #ff5f6d, #ffc371);
		justify-content: center;
		align-items: center;
	}
</style>
