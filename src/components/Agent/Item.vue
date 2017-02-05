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
				<span class="btn" @click="add">
					Specify Resources
				</span>
				<div class="sep">
					Resources: 
					<span v-for="item in agent.resources" class="tag" @click="del($index)">{{item}}</span > 
				</div>
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
  methods: {
    add () {

    },
    del (index) {
      this.agent.resources && this.agent.resources.splice(index, 1)
    }
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
		
		.meta {
			margin-top: 20px;
			display: flex;
			
			.tag {
				margin-left: 15px;
				cursor: pointer;
				
				&:after {
					content: "x";
					border: 1px solid #ddd;
					color: #ddd;
					border-radius: 50%;
					height: 14px;
					width: 14px;
					display: inline-block;
					font-size: 10px;
					margin-left: 8px;
				}
			}
		}
		
		.btn {
			cursor: pointer;
		}
	}
</style>