<script>
	export let cardAttributes = [];
	import '@fontsource/roboto/900.css';
</script>

<div class="wrapper" style="place-self:end">
	{#each cardAttributes as attribute}
		<div class="column">
			<div class="icon">
				<svg xmlns="http://www.w3.org/2000/svg" width="25px" height="25px" viewBox="0 0 700 700"
					><path
						d="M346.71 155.52a8.766 8.766 0 0 0-4.559 4.238l-35.793 72.48-80.137 11.594h.004a8.756 8.756 0 0 0-7.05 5.965 8.75 8.75 0 0 0 2.23 8.957l57.934 56.441-13.703 79.676a8.738 8.738 0 0 0 3.488 8.543 8.75 8.75 0 0 0 9.211.668l71.633-37.602 71.664 37.63a8.76 8.76 0 0 0 9.23-.661 8.733 8.733 0 0 0 3.481-8.566l-13.68-79.672 57.938-56.395.004-.004a8.735 8.735 0 0 0 2.227-8.95 8.755 8.755 0 0 0-7.047-5.964l-80.094-11.645-35.81-72.488a8.761 8.761 0 0 0-11.171-4.246zm3.313 27.848 29.991 60.73h.004a8.748 8.748 0 0 0 6.59 4.805l67.086 9.734-48.555 47.242a8.747 8.747 0 0 0-2.527 7.773l11.44 66.738-59.968-31.523v-.003a8.77 8.77 0 0 0-8.164-.036l-60.031 31.477 11.488-66.71.004.003a8.74 8.74 0 0 0-2.528-7.699l-48.527-47.305 67.098-9.71v-.005a8.753 8.753 0 0 0 6.602-4.78z"
					/><path
						d="M174.98 61.25c-24.086 0-43.73 19.645-43.73 43.73v350.04c0 24.086 19.645 43.73 43.73 43.73h350.04c24.086 0 43.73-19.645 43.73-43.73V104.98c0-24.086-19.645-43.73-43.73-43.73zm0 17.504h350.04c14.695 0 26.227 11.531 26.227 26.227v350.04c0 14.695-11.531 26.227-26.227 26.227H174.98c-14.695 0-26.289-11.531-26.289-26.227v-350.04c0-14.695 11.594-26.227 26.289-26.227z"
					/></svg
				>
			</div>
			<div class="attributes">
				<p class="title">{attribute.title}</p>
				<p class="desc">{attribute.desc}</p>
			</div>
		</div>
	{/each}
</div>

<style>
	.wrapper {
		display: flex;
		flex-direction: column;
		max-width: 300px;
		row-gap: 0.5rem;
		padding-block-end: 2rem;
	}
	.column {
		display: grid;
		grid-template-columns: auto 1fr;
		grid-template-areas: 'icon attributes';
		column-gap: 0.5rem;
	}

	.icon {
		grid-area: icon;
		place-self: center;
		align-self: baseline;
	}
	.attributes {
		display: flex;
		flex-direction: column;
		grid-area: attributes;
		place-self: center;
		margin-right: auto;
		row-gap: 0.25rem;
	}
	.title {
		font-size: 12px;
		font-weight: 900;
		font-family: 'Roboto', sans-serif;
		margin: 0;
	}
	.desc {
		font-size: 12px;
		font-weight: 400;
		font-family: 'Roboto', sans-serif;
		margin: 0;
		max-width: 220px;
	}
</style>
