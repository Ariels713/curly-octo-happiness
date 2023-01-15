<script>
	export let cardValue = 1;
	import '@fontsource/roboto/900.css';
</script>

<div class="stack" style="place-self:end start">
	<span>{cardValue}</span>
    <p class="value">Value</p>
</div>

<style>
	.stack {
		display: flex;
		flex-direction: column;
        gap: 1rem;
        align-items: center;
		max-width: 5ch;
		font-weight: 900;
		font-family: 'Roboto', sans-serif;
		font-size: 96px;
		padding-inline: 1.5rem;
		padding-block-end: 1rem;
        line-height: .5;
	}
    .value  {
        font-size: 12px;
        font-weight: 900;
        font-family: 'Roboto', sans-serif;
    }
</style>
