<template>
	<div>
<MyChildComponent></MyChildComponent>
//Namedslots
	<ArticleTemplate>
		<template #header>
			<h1>Page Header</h1>
		</template>
		<h3>VUE CLI</h3>
		<p>Article Content</p>

		<template #footer>
			<p>Page Footer</p>
		</template>
	</ArticleTemplate>

//Scoppedslots
		<FruitList :fruits="fruitsOfTheNinja">
			<template #default="{ fruit, slice }">
				{{ fruit.name }}
				<button @click="slice(fruit.id)">
					⚔️ Style Slicing
				</button>
			</template>
		</FruitList>
	</div>
</template>

<script>
import Slots from './components/Slots.vue'
import Namedslots from './components/Namedslots.vue'
import Scoppedslots from './components/Scoppedslots.vue'
export default {
	data () {
		return {
			fruitsOfTheNinja: [
				{
					id: 1,
					name: '🍋Lemon'
				},
				{
					id: 2,
					name: '🥝Kiwi',
					recipe: 'Kiwi, Baijiu & Red Date Yoghurt Cocktail 🍸'
				},
				{
					id: 3,
					name: '🍑Peach'
				},
				{
					id: 4,
					name: '🍌Banana'
				},
				{
					id: 5,
					name: '🍎Apple'
				}
			]
		}
	},
	components: {
		'MyChildComponent': Slots,
		'ArticleTemplate': Namedslots,
		'FruitList': Scoppedslots
	}
}
</script>
