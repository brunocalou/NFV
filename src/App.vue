<template>
	<div id="app">
		<home></home>
		<easter-egg></easter-egg>
	</div>
</template>

<script>
import Home from './components/Home.vue'
import EasterEgg from './components/EasterEgg/EasterEgg.vue'

export default {
	name: 'app',
	components: {
		Home, EasterEgg
	}
}
</script>

<style lang="sass">
  
</style>
