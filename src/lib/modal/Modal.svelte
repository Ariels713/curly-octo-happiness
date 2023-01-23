<script>
	import { createEventDispatcher, onDestroy } from 'svelte';
	import Card from '../card/card.svelte';
	import Andre from '$lib/data/Andre.js';
	import AndreImage from '$lib/assets/images/Andre_shin.png';
	import andreBG from '$lib/assets/svg/andreBG.svg';
	const dispatch = createEventDispatcher();
	const close = () => dispatch('close');

	let modal;

	const handle_keydown = (e) => {
		if (e.key === 'Escape') {
			close();
			return;
		}

		if (e.key === 'Tab') {
			// trap focus
			const nodes = modal.querySelectorAll('*');
			const tabbable = Array.from(nodes).filter((n) => n.tabIndex >= 0);

			let index = tabbable.indexOf(document.activeElement);
			if (index === -1 && e.shiftKey) index = 0;

			index += tabbable.length + (e.shiftKey ? -1 : 1);
			index %= tabbable.length;

			tabbable[index].focus();
			e.preventDefault();
		}
	};

	const previously_focused = typeof document !== 'undefined' && document.activeElement;

	if (previously_focused) {
		onDestroy(() => {
			previously_focused.focus();
		});
	}
</script>

<svelte:window on:keydown={handle_keydown} />

<div class="modal-background" on:click={close} />

<div class="modal" role="dialog" aria-modal="true" bind:this={modal}>
	<slot name="header" />
	<slot />


	<!-- svelte-ignore a11y-autofocus -->
</div>
<button autofocus on:click={close}>close modal</button>

<style>
	.modal-background {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0, 0, 0, 0.3);
	}

	.modal {
		position: absolute;
		left: 50%;
		top: 35%;
		width: calc(100vw - 4em);
		max-width: 52em;
		max-height: calc(100vh - 4em);
		overflow: auto;
		transform: translate(-50%, -50%);
		padding: 2rem;
		border-radius: 0.2em;
		
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

		--min: 10ch;
		--gap: 1rem;

		display: flex;
		flex-wrap: nowrap;
		gap: var(--gap);
        justify-content: center;
	}

	.modal > * {
		flex: 1 1 var(--min);
	}

	button {
		display: block;
        position: absolute;
        top: 0;
        left: 0;
	}
</style>
