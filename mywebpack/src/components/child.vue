<template>
	<div id="">
		<p>{{cmsg}}</p>
		<p><button @click="fn">click</button></p>
	</div>
</template>
<script type="text/javascript">
	export default{
		name:'child',
		data(){
			return{
				zmsg:'子内容'
			}
		},
		props:['cmsg'],
		methods:{
			fn(){
				this.$emit('change',this.zmsg)
			}
		}
	}
</script>
<style>
	
</style>