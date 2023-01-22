<script>
	import Card from '$lib/card/Card.svelte';
	import Andre from '$lib/data/Andre.js';
	import AndreImage from '$lib/assets/images/Andre_shin.png';
	import andreBG from '$lib/assets/svg/andreBG.svg';
	import Arya from '../lib/data/Arya';
	import aryaBG from '$lib/assets/svg/aryaBG.svg';
	import AryaImage from '../lib/assets/images/Arya_Knox.png';
	import Barrington from '$lib/assets/images/Barrington.png'
	import bjBG from '$lib/assets/svg/bjBG.svg';

	let toggle = false;

	function handleClick() {
		toggle = !toggle;
	}
</script>

<div class="background">
	<div data-toggle={`${toggle}`} class="board">
		<Card {...Andre} playerImage={AndreImage} bg={andreBG} />
		<Card {...Arya} playerImage={AryaImage} bg={aryaBG} />
		<Card {...Arya} playerImage={Barrington} bg={bjBG} />
	</div>

	<div class="btnWrapper">
		<button on:click={handleClick}>Toggle</button>
	</div>
</div>

<style>
	.board {
		min-width: 700px;
		margin-inline: auto;
		--min-column-width: min(320px, 100%);
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(var(--min-column-width), 1fr));
		gap: 16px;
		padding: 16px;
		transform: scale(1) rotateX(0deg) rotateZ(0deg);
		transition: transform 0.5s ease-in-out;
	}
	[data-toggle='true'] {
		transform:  rotateX(56deg) translate(-100px, -300px) scale(0.6) rotateZ(314deg);
	}
	.background {
		position: relative;
		font-family: sans-serif;
		display: grid;
		place-content: center;
		background: linear-gradient(
			to right,
			hsl(174.93, 100%, 86.08%) 0%,
			hsl(170.29, 94.01%, 83.65%) 5.9%,
			hsl(167.05, 90.37%, 81.62%) 11.7%,
			hsl(164.73, 88.01%, 79.94%) 17.5%,
			hsl(163.04, 86.42%, 78.57%) 23.3%,
			hsl(161.77, 85.29%, 77.42%) 29%,
			hsl(160.75, 84.43%, 76.42%) 34.9%,
			hsl(159.86, 83.71%, 75.49%) 40.9%,
			hsl(159.01, 83.05%, 74.51%) 47.1%,
			hsl(158.1, 82.38%, 73.39%) 53.6%,
			hsl(157.09, 81.67%, 72%) 60.3%,
			hsl(155.95, 80.93%, 70.18%) 67.4%,
			hsl(154.68, 80.19%, 67.73%) 74.8%,
			hsl(153.42, 79.6%, 64.29%) 82.7%,
			hsl(152.55, 79.44%, 59.11%) 91.1%,
			hsl(156, 100%, 45.1%) 100%
		);
		min-height: 100vh;
	}
	.btnWrapper {
		position: absolute;
		left: 20px;
		top: 20px;
	}
</style>
