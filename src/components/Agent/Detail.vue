<template>
	<div class="detail">
		<section class="summary">
			<h3>Summary</h3>
		</section>

		<section class="history">
			<h3>History</h3>
		</section>
	</div>
</template>

<script>
export default {
  name: 'AgentDetail',

  data () {
    return {

    }
  }
}
</script>

<style lang="stylus" scoped>
	.detail {
		section {
			display: flex;
			padding: 20px 10px;
			
			h3 {
				border-bottom: 2px solid #ddd;
				width: 100%;
				text-align: left;
				padding-bottom: 10px;
			}
		}
	}
</style>