<script>
	export let offence = 1;
	export let defence = 1;
	import '@fontsource/roboto/900.css';
</script>

<div class="vertical" style="place-self:start end">
	<span>OFF</span>
	<div class="value">{offence}</div>
	<div class="divider" />
	<span>DEF</span>
	<div class="value">{defence}</div>
</div>

<style>
	.vertical {
		display: flex;
		flex-direction: column;
		max-width: 5ch;
		padding-inline: 1rem;
		padding-block: 1rem;
		align-items: center;
		font-weight: 900;
		font-family: 'Roboto', sans-serif;
	}

	span {
		font-size: 12px;
		font-weight: 900;
		font-family: 'Roboto', sans-serif;
	}

	.value {
		font-family: 'Roboto', sans-serif;
		font-weight: 900;
		font-size: 38px;
		line-height: 0.9;
	}

	.divider {
		height: 15px;
		width: 100%;
		background: black;
		clip-path: polygon(0 48%, 100% 48%, 100% 52%, 0 52%);
	}
</style>
