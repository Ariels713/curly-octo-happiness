<script>
	import Player from '$lib/assets/images/Andre_shin.png';
</script>

<svg
	class="bubbles"
	xmlns="http://www.w3.org/2000/svg"
	viewBox="0 0 175 200"
	><g fill="#cbfbe0"
		><path
			d="M11.263 84.647c0-33.232 26.94-60.171 60.172-60.171s60.171 26.94 60.171 60.171c0 33.232-26.939 60.172-60.171 60.172s-60.172-26.94-60.172-60.172Z"
		/><path
			d="M82.796 142.694c0-22.712 18.412-41.123 41.124-41.123 22.712 0 41.124 18.411 41.124 41.123 0 22.712-18.412 41.124-41.124 41.124-22.712 0-41.124-18.412-41.124-41.124Z"
		/></g
	></svg
>

<img alt="Andre Shin" src={Player} />

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
