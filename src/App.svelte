<script>
	let people = [
		{name: 'abdul', beltColour: 'black', age: 25, id:1},
		{name: 'abizar', beltColour: 'orange', age: 23, id:2},
		{name: 'anissa', beltColour: 'purple', age: 20, id:3}
	];
</script>

<main>
	{#each people as person (person.id)}
		<div>
			<h4>{person.name}</h4>
			<p>{person.age} years old, {person.beltColour} belt.</p>
		</div>
	{:else}
		<p>There are no people to showw ....</p>
	{/each}	
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>