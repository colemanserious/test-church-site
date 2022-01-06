<template>
  <div>
	<h1>Services</h1>
	<ul>
		<li v-for="service of services" :key="service.slug">
			<NuxtLink :to="{ name: 'services-slug', params: { slug: service.slug } }">
				<h2>{{ service.title }}</h2>
				<p>{{ service.description }}</p>
			</NuxtLink>
		</li>
	</ul>
  </div>
</template>

<script>
	export default {
		name: 'ServicePage',
		async asyncData({ $content, params }) {

			const services = await $content('sermons')
				.only(['title', 'slug', 'description'])
				.sortBy('createdAt', 'asc')
				.fetch()

			return {
				services
			}
		}
	}
</script>
