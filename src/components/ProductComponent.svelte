<script lang="ts">
	const mockdata = [
		{ label: 'Developer: The Game Collective' },
		{ label: 'Genre: RPG Maker Horror' },
		{
			label:
				'Description: A recently deceased young man learns he can quickly acquire good karma by helping a local priest.'
		},
		{ label: 'Release Date: March 2020' },
		{ label: 'Source Code Included!' }
	];

	let gameDetails = null;

	function setGameDetails(gameName: string) {
		if (gameName === 'Abyss of the Self') {
			gameDetails = [
				{ label: 'Developer: The Game Collective' },
				{ label: 'Genre: RPG Maker Horror' },
				{
					label:
						'Description: A recently deceased young man learns he can quickly acquire good karma by helping a local priest.'
				},
				{ label: 'Release Date: March 2020' },
				{ label: 'Source Code Included!' }
			];
		} else {
			gameDetails = null;
		}
	}
	import myImage from '../assets/AbyssOfTheSelfScreenshot3.png';
</script>

<div class="card w-80 mx-auto font-mono">
	<img src={myImage} alt="Abyss of The Self Screenshot" class="p-4" />
	<hr />

	<div class="flex justify-between items-center p-4">
		<div>
			<b>Abyss of the Self</b>
			<div class="text-xs opacity-70">Explore the mysteries...</div>
		</div>
		<div class="badge variant-ghost-tertiary">Vertical Slice</div>
	</div>
	<hr />
	{#if gameDetails}
		<div class="p-4 border-t border-surface-300-600-token space-y-4">
			<div class="uppercase opacity-70 font-bold text-sm">Game Details</div>
			<div class="">
				{#each gameDetails as item}
					<div class="inline-flex px-1 text-sm items-center">
						<div class="ml-1">{item.label}</div>
					</div>
				{/each}
			</div>
		</div>
	{:else}
		<div class="p-4 border-t border-surface-300-600-token space-y-4">
			<div class="uppercase opacity-70 font-bold text-sm">Details</div>
			<div class="">
				{#each mockdata as item}
					<div class="inline-flex px-1 text-sm items-center">
						<div class="ml-1">{item.label}</div>
					</div>
				{/each}
			</div>
		</div>
	{/if}
	<hr />
	<div class="flex justify-between p-4 gap-8">
		<div>
			<div class="font-semibold text-2xl">$1.99</div>
			<div class="text-sm opacity-70">PC, Mac, Linux</div>
		</div>
		<button
			class="btn btn-sm variant-filled-primary w-full"
			on:click={() => setGameDetails('Abyss of the Self')}>Buy now</button
		>
	</div>
</div>
