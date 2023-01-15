<script>
	export let ShotZone = [];
	import '@fontsource/roboto/900.css';
</script>

<div class="stack" style="place-self: center end">
	<div class="vertical-text">SHOT ZONE</div>
	<!-- map over ShotZone, return a div with each value, if it's the 3rd value, return a div with a class of bonus -->
	{#each ShotZone as value, i}
		{#if i === 2}
			<div class="bonus">{value}</div>
		{:else}
			<div class="value">{value}</div>
		{/if}
	{/each}
</div>

<style>
	.vertical-text {
		writing-mode: vertical-lr;
		transform: rotate(180deg);
		font-size: 10px;
		font-weight: 900;
		padding-block: 1rem;
		font-weight: 900;
		font-family: 'Roboto', sans-serif;
	}
	.stack {
		display: flex;
		flex-direction: column;
		row-gap: 0.5rem;
		align-items: center;
		justify-content: center;
		padding-block-start: 2.5rem;
		font-weight: 900;
		font-family: 'Roboto', sans-serif;
	}

	.value {
		display: grid;
		place-items: center;
		width: 20px;
		height: 20px;
		border: 1.5px solid black;
		border-radius: 50%;
		line-height: 0;
	}
	.bonus {
		display: grid;
		place-items: center;
		width: 30px;
		height: 30px;
		border: 1.5px solid black;
		border-radius: 50%;
		line-height: 0;
	}
</style>
