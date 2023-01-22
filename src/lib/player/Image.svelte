<script>
	export let playerImage = '';
	export let bg;
</script>

<img alt="Andre Shin" src={bg} class=bubbles/>
<img alt="Andre Shin" src={playerImage} />

<style>
	img {
		object-fit: cover;
		object-position: 50% 50%;
		max-width: 260px;
		padding-block-end: 110px;
	}
	.bubbles {
		padding-block-end: 110px;
	}
</style>
