<template>
	<div>
		<h1>Gallery: </h1>
		<router-link v-for="(item, index) of arrPhotos" :key="index" :to="{name: 'photos', params: {id: item}}">
			<button>Photo {{item}}</button>
		</router-link>
		<Photo/>

		<button @click="home">Home</button>
	</div>
</template>

<script>
	import Photo from '../components/Photo';

	export default {
		name: 'Photos',
		components: { Photo },
		data() {
			return {
				arrPhotos: [1, 2, 3]
			};
		},
		methods: {
			home() {
				this.$router.push( '/' );
			}
		}
	};
</script>

<style scoped>

</style>
