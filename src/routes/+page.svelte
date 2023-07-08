<script>
	let todos = [];
	let todoInput = '';
	let interaction = 0;
	let count = 0;
	function addTodo() {
		if (todoInput === '') return;
		todos = [...todos, todoInput];
		todoInput = '';
	}
</script>

<main>
	<div class="input">
		<form on:submit={() => addTodo()}>
			<input bind:value={todoInput} type="text" placeholder="Add a new todo" />
			<button type="submit">Add Todo</button>
		</form>
	</div>
	<div>
		{#each todos as todo}
			<div>
				{todo}
				<button on:click={() => (todos = todos.filter((o) => o !== todo))}>Delete</button>
			</div>
		{/each}
	</div>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		max-width: 1400px;
		margin: 0 auto;
	}
	h1 {
		text-align: center;
		font-size: 3rem;
		color: #000000;
		margin: 0;
		padding: 0;
	}
	input {
		width: 100%;

		padding: 10px;
		border-radius: 5px;
		border: 1px solid #00000023;
	}
	button {
		width: 100%;
	}
	button:hover {
		transform: scale(0.95);
	}
	button:active {
		transform: scale(0.9);
	}

	.input {
		display: flex;
		flex-direction: column;
		gap: 10px;
		align-items: center;
		justify-content: center;
	}
</style>
