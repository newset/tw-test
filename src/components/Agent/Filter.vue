<template>
	<div class="filter">
		<h3>Agent</h3>
		<ul>
			<li>All</li>
			<li v-for="item in categories" :class="{active: item==current}">{{item}}</li>
		</ul>
	</div>
</template>

<script>
const categories = ['physical', 'virtual']

export default {
  name: 'AgentFilter',
  data () {
    return {
      categories: categories,
      current: 'physical'
    }
  }
}
</script>

<style lang="stylus" scoped>
	@import '../../assets/css/var'
	.filter {
		display: flex;
		h3 {
			line-height: 3em;
			margin: 0px 20px;
		}
	}

	ul {
		display: flex;

		li {
			margin: 10px;
			padding: 5px 20px;
			border: 2px solid #888;
			border-radius: 20px;
			
			&.active {
				background-color: #ddd;
			}
		}
	}
</style>