<template>
	<view>
		组件test
	</view>
</template>

<script>
	export default {
		name: "test",
		data() {
			return {

			};
		},
		beforeCreate() {
			console.log('component beforeCreate')
		},
		created() {
			console.log('component created')
		},
		mounted() {
			console.log('component mounted')
		},
		destroyed() {
			console.log('component destroyed')
		}

	}
</script>

<style>

</style>
