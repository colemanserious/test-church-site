<script>
	export default {
		async asyncData({ $content, params }) {
			const post = await $content('sermons', params.slug).fetch()
			const [prev, next] = await $content('sermons')
			 	.only(['title', 'slug'])
				.sortBy('createdAt', 'asc')
				.surround(params.slug)
				.fetch()

			return { post, prev, next }
		},

		methods: {
			formatDate(date) {
				const options = { year: 'numeric', month: 'long', day: 'numeric' }
				return new Date(date).toLocaleDateString('en', options)
			}
		}
	}
</script>

<template>
	<post>
		<h1>Title: {{ post.title }}</h1>
		<div>
		<h3>Verses</h3>
		<p v-for="(verse, index) in post.verses" :key="index">{{ verse }}</p> 
		</div>

		<p>Service information last update: {{ formatDate(post.updatedAt) }} </p>
		<nuxt-content :document="post" />

		<prev-next :prev="prev" :next="next" />
	</post>
</template>



