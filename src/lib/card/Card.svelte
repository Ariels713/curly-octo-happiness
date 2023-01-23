<script>
	import Image from '$lib/player/Image.svelte';
	import Name from '$lib/player/Name.svelte';
	import Ability from '../player/Ability.svelte';
	import ShotZones from '../player/ShotZones.svelte';
	import Value from '../player/Value.svelte';
	import Attribules from '../player/Attribules.svelte';

	export let playerName = 'Johnny Bravo';
	export let playerAbility = { offence: 1, defence: 1 };
	export let ShotZone = [];
	export let cardValue = 1;
	export let cardAttributes = [];
	export let playerImage = '';
	export let bg = '';
</script>


<div class="card">
	<div class="layer" />
	<div class="layer" />
	<div class="layer" />
	<Image {playerImage} {bg} />
	<Name {playerName} />
	<Ability {...playerAbility} />
	<ShotZones {ShotZone} />
	<Value {cardValue} />
	<Attribules {cardAttributes} />
</div>

<style>
	:root {
		--shadow-color: 0deg 0% 0%;
		--shadow-elevation-medium: -0.5px 0.6px 0.7px hsl(var(--shadow-color) / 0.26),
			-1.3px 1.5px 1.8px -1.3px hsl(var(--shadow-color) / 0.21),
			-4.1px 5px 5.9px -2.6px hsl(var(--shadow-color) / 0.16),
			-11.3px 14px 16.5px -3.9px hsl(var(--shadow-color) / 0.12);
		--shadow-elevation-high: -0.5px 0.6px 0.7px hsl(var(--shadow-color) / 0.24),
			-2px 2.5px 2.9px -0.6px hsl(var(--shadow-color) / 0.22),
			-4.3px 5.3px 6.2px -1.1px hsl(var(--shadow-color) / 0.2),
			-8.5px 10.5px 12.4px -1.7px hsl(var(--shadow-color) / 0.17),
			-15.7px 19.5px 22.9px -2.2px hsl(var(--shadow-color) / 0.15),
			-27.3px 33.7px 39.7px -2.8px hsl(var(--shadow-color) / 0.13),
			-44.3px 54.7px 64.4px -3.3px hsl(var(--shadow-color) / 0.11),
			-67.8px 83.8px 98.6px -3.9px hsl(var(--shadow-color) / 0.09);
	}

	div {
		transform-style: preserve-3d;
		position: relative;
		display: grid;
		grid-template-areas: 'Stack';
		place-items: center;
		width: 350px;
		height: 500px;
		border-radius: 1rem;
		background-color: #fff;
	}

	:global(.card > *) {
		grid-area: Stack;
		place-self: var(--place-self, center);
		align-self: var(--align-self, var(--place-self));
		justify-self: var(--justify-self, var(--place-self));
	}
	.layer {
		position: absolute;
		background-color: transparent;
		position: absolute;
		width: 100%;
		height: 100%;
		transition: 1s;
		border-radius: inherit;
	}
	.layer:nth-child(1) {
		background-color: #1b9956;
		transform: translate3d(-1px, 1px, -1px);
	}
	.layer:nth-child(2) {
		background-color: #1b9956;
		transform: translate3d(-2px, 2px, -2px);
	}
	.layer:nth-child(3) {
		background-color: #1b9956;
		transform: translate3d(-3px, 3px, -3px);
	}
</style>
