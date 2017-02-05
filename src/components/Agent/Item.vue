<template>
	<div class="item {{agent.status}}">
		<span class="round"></span>
		<div class="info">
			<div class="basic">
				<h3>
					{{agent.host}}
				</h3>
				<span class="sep">{{agent.status}}</span>
				<span class="sep">{{agent.addr}}</span>
				<span class="sep">{{agent.dir}}</span>
			</div>
			<div class="meta">
				
			</div>
		</div>
	</div>
</template>

<script>
export default {
  name: 'AgentItem',
  props: ['agent'],
  data () {
    return {
    }
  },
  mounted () {
    console.log(this.agent)
  }
}
</script>

<style lang="stylus" scoped>
	.item {
		display: flex;
		margin: 20px;
		padding: 20px;
		border: 2px solid #ddd;
		border-radius: 4px;

		.round {
			width: 50px;
			height: 50px;
			border-radius: 50%;
			background-color: #ddd;
			margin-right: 20px;
		}
		
		.sep:before {
			content: "|"
			padding: 0px 10px;
			color: #ddd;
		}
		
		.sep {
			margin-left: 0px;
		}
		
		.basic {
			flex: 1;
			display: flex;
		}
	}
</style>