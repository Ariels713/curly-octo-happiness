
<script> 
    import Image from '$lib/player/Image.svelte';
    import Name from '$lib/player/Name.svelte';
	import Ability from '../player/Ability.svelte';
	import ShotZones from '../player/ShotZones.svelte';
    import Value from '../player/Value.svelte';
    import Attribules from '../player/Attribules.svelte';

    export let playerName = "Johnny Bravo";
    export let playerAbility = {offence: 1, defence: 1};
    export let ShotZone = []
    export let cardValue = 1;
    export let cardAttributes = [];

</script>

<div class="card">
    <Image/>
    <Name playerName={playerName}/>
    <Ability {...playerAbility}/>
    <ShotZones ShotZone={ShotZone} />
    <Value cardValue={cardValue}/>
    <Attribules cardAttributes={cardAttributes}/>
</div>

<style>
	div {
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
</style>
