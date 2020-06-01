<template>
	<div class="my-child-component">
  <ul>
		<li v-for="fruit in fruits" :key="fruit.id">
			<slot :fruit="fruit" :slice="slice" />
		</li>
	</ul>
	</div>
</template>

<script>
export default {
	name: 'Scoppedslots',
	props: {
		fruits: {
			type: Array,
			required: true
		}
	},

	methods: {
		slice (id) {
			// ... handles the fruit slicing Ninja style!
		}
	}
}
</script>
