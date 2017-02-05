<template>
	<div class="detail-container">
		<section class="summary">
			<h3>Summary</h3>
			<ul>
				<li>Building
					<span>2</span>
				</li>
				<li>Idel
					<span>2</span>
				</li>
			</ul>
		</section>

		<section class="history">
			<h3>History</h3>
			<ul>
				<li v-for="item in history" track-by="$index">
					oei12z102/Accept_test
				</li>
			</ul>
		</section>
	</div>
</template>

<script>
export default {
  name: 'AgentDetail',

  data () {
    return {
      history: 'a'.repeat(10).split('')
    }
  }
}
</script>

<style lang="stylus" scoped>
	.detail-container {
		border: none;
		
		section {
			display: flex;
			padding: 20px 10px;
			flex-direction: column;
			
			h3 {
				border-bottom: 2px solid #ddd;
				width: 100%;
				text-align: left;
				padding-bottom: 10px;
			}
			
			ul {
				display: flex;
				flex-direction: column;
				
				li {
					text-align: left;
					padding: 10px;
					color: #999;
					
					span {
						float: right;
					}
				}
			}
		}
	}
</style>