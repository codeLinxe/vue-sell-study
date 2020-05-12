<template>
	<div id="app" @touchmove.prevent>
		<v-header :seller="seller"></v-header>
	</div>
</template>

<script>
	import VHeader from 'components/v-header/v-header'
	
	export default {
		name: 'App',
		components: {
			VHeader
		}
	}
</script>

<style lang="stylus">
</style>
