<template>
	<router-view></router-view>
</template>

<script>
	import Vue from 'Vue';

	export default {
		template: __template__,
		components: {},
		data: function() {
			return {
				user: this.$store.state.user
			}
		}
	};
</script>

<style>
	main {
		padding: 2.5rem 0;
	}
	.content {
		color: #999;
	}
	.card_head {
		font-weight: 600;
		text-align: center;
	}
	header h3 {
		line-height: 2.5rem;
		padding: 0 0.5rem;
	}
	header h3 .fr {
		font-weight: normal;
		font-size: 0.75rem;
	}
</style>
