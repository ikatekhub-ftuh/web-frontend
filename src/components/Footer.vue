<template>
	<div class="col-span-12">
		<Card class="col-span-12 shadow-md">
			<template #content>
				<div class="flex items-center justify-between">
					<p class="text-2xl font-bold flex items-center gap-2">ANTEK HUB</p>
					<ul class="flex gap-5">
						<li v-for="item in list" :key="item.name"><RouterLink :to="item.link" class="hover:underline">{{ item.name }}</RouterLink></li>
					</ul>
				</div>
				<p class="text-center text-sm text-gray-600">Copyright © 2024 ANTEK HUB. All rights reserved.</p>
			</template>
		</Card>
	</div>
</template>

<script>
export default {
	name:'Footer',
	inject:['default'],
	data() {
		return {
			list: [
				{
					name: 'Privacy Policy',
					link: '/privacy-policy/en',
				},
			]
		}
	},
	methods: {
	},
	mounted() {
	},
}
</script>