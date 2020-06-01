<template>
	<div class="my-child-component">
		<header>
			<slot name="header" />
		</header>

		<main>
			<img src="images.png" />
			<slot />
			<AuthorComponent />
		</main>

		<footer>
			<slot name="footer" />
		</footer>
	</div>
</template>

<script>
export default {
	name: 'Namedslots'
}
</script>
