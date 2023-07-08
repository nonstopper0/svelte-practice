<header>
	<nav>
		<a href="/">Todo List</a>
		<a href="/page">Page</a>
		<a href="/contact">Contact</a>
	</nav>
</header>

<slot />

<style>
	nav {
		display: flex;
		justify-content: center;
		gap: 30px;
		align-items: center;
		color: #ffffff;
		padding: 1rem;
	}
	a {
		text-decoration: none;
		color: #ffffff;
	}
</style>
