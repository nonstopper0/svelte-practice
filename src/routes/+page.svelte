<script>
	let todos = [];
	let todoInput = '';

	let count = 0;
	function addTodo() {
		count++;
		todos = [...todos, todoInput];
		todoInput = '';
	}
</script>

<main>
	<h1>To Do App Svelte</h1>
	<input bind:value={todoInput} type="text" placeholder="Add a new todo" />
	<button on:click={() => addTodo()}>Clicked {count}</button>
	<div>
		{#each todos as todo}
			<p>{todo}</p>
		{/each}
	</div>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	h1 {
		text-align: center;
		font-size: 3rem;
		color: #000000;
		margin: 0;
		padding: 0;
	}
	button {
		background-color: #000000;
		color: #ffffff;
		border: none;
		padding: 1rem;
		font-size: 1.5rem;
		border-radius: 0.5rem;
	}
	button:hover {
		transform: scale(0.95);
	}
	button:active {
		transform: scale(0.9);
	}
</style>
