<script>
	import Card from '../card/card.svelte';
	import Andre from '$lib/data/Andre.js';
	import AndreImage from '$lib/assets/images/Andre_shin.png';
	import andreBG from '$lib/assets/svg/andreBG.svg';
</script>

<div class="stack">
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="card" />
	<div class="player">
		<Card {...Andre} playerImage={AndreImage} bg={andreBG} />
	</div>
</div>

<style>
	.stack {
 --shadow-color: 160deg 56% 33%;
  --shadow-elevation-low:
    -1px 1px 1.6px hsl(var(--shadow-color) / 0.55),
    -1.9px 1.9px 3px -1.3px hsl(var(--shadow-color) / 0.53),
    -5px 5px 7.8px -2.7px hsl(var(--shadow-color) / 0.51);
  --shadow-elevation-medium:
    -1px 1px 1.6px hsl(var(--shadow-color) / 0.58),
    -3.8px 3.8px 5.9px -0.9px hsl(var(--shadow-color) / 0.56),
    -10px 10px 15.6px -1.8px hsl(var(--shadow-color) / 0.55),
    -25px 25px 39px -2.7px hsl(var(--shadow-color) / 0.53);
  --shadow-elevation-high:
    -1px 1px 1.6px hsl(var(--shadow-color) / 0.54),
    -7.9px 7.9px 12.3px -0.4px hsl(var(--shadow-color) / 0.53),
    -15.2px 15.2px 23.7px -0.8px hsl(var(--shadow-color) / 0.52),
    -25.6px 25.6px 39.9px -1.1px hsl(var(--shadow-color) / 0.52),
    -41.7px 41.7px 65px -1.5px hsl(var(--shadow-color) / 0.51),
    -66px 66px 102.9px -1.9px hsl(var(--shadow-color) / 0.5),
    -101.3px 101.3px 157.9px -2.3px hsl(var(--shadow-color) / 0.49),
    -150px 150px 233.9px -2.7px hsl(var(--shadow-color) / 0.48);
		width: 350px;
		height: 500px;
		border-radius: 1rem;
		box-shadow: var(--shadow-elevation-high);
		/* background-color: #1b9956; */
	}

	.card {
		position: absolute;
		width: 100%;
		height: 100%;
		transition: 1s;
		border-radius: inherit;
	}

	.player {
		position: absolute;
		top: -50px;
		left: 50px;
	}

	.card:nth-child(1) {
		background-color: hsla(148, 70%, 50%, 1);
		transform: translate3d(5px, -5px, -1px);
	}
	.card:nth-child(2) {
		background-color: hsla(148, 70%, 55%, 1);
		transform: translate3d(10px, -10px, -2px);
	}
	.card:nth-child(3) {
		background-color: hsla(148, 70%, 60%, 1);
		transform: translate3d(15px, -15px, -3px);
	}
	.card:nth-child(4) {
		background-color: 6hsla (148, 70%, 65%, 1);
		transform: translate3d(20px, -20px, -4px);
	}
	.card:nth-child(5) {
		background-color: hsla(148, 70%, 70%, 1);
		transform: translate3d(25px, -25px, -5px);
	}
	.card:nth-child(6) {
		background-color: hsla(148, 70%, 75%, 1);
		transform: translate3d(30px, -30px, -6px);
	}
	.card:nth-child(7) {
		background-color: hsla(148, 70%, 80%, 1);
		transform: translate3d(35px, -35px, -7px);
	}
	.card:nth-child(8) {
		background-color: hsla(148, 70%, 85%, 1);
		transform: translate3d(40px, -40px, -8px);
	}
	.card:nth-child(9) {
		background-color: hsla(148, 70%, 90%, 1);
		transform: translate3d(45px, -45px, -9px);
	}
	.card:nth-child(10) {
		background-color: hsla(148, 70%, 95%, 1);
		transform: translate3d(50px, -50px, -10px);
	}
</style>
