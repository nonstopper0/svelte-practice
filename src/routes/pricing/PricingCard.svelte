<script>
	export let tier;
</script>

<div class="card" on:mouseover={hover} on:mouseout={unhover}>
	<img src={tier.icon} alt={tier.name} />
	<h2>{tier.name}</h2>
	<h1>${tier.price}</h1>
	<ul>
		{#each tier.features as feature (feature)}
			<li>{feature}</li>
		{/each}
	</ul>
</div>

<style>
	.card {
		padding: 20px;
		background: rgba(255, 255, 255, 0.1);
		backdrop-filter: blur(10px);
		border-radius: 15px;
		color: #fff;
		text-align: center;
		box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
		transition: transform 0.5s;
	}
	.card:hover {
		transform: scale(1.05);
	}
	.card img {
		width: 50px;
		height: 50px;
	}
	.card h2 {
		font-family: 'Poppins', sans-serif;
		font-size: 24px;
		margin: 20px 0;
	}
	.card h1 {
		font-family: 'Poppins', sans-serif;
		font-size: 48px;
		margin: 20px 0;
	}
	.card ul {
		list-style-type: none;
		padding: 0;
		font-family: 'Poppins', sans-serif;
	}
</style>
