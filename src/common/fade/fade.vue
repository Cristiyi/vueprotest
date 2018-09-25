<template>
	<transition>
		<slot></slot>
	</transition>
</template>	

<script type="text/javascript">
	export default {
		name: 'Fade',
	}
</script>

<style type="text/css" lang="stylus" scoped>
	.v-enter, .v-leave-to
		opacity: 0
	.v-enter-active, .v-leave-active
		transition: opacity .2s
</style>