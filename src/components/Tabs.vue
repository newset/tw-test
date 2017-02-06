<template>
	<div class="tabs">
		<h3>Cruise</h3>
		<ul>
			<li><a href="#">Dashboard</a></li>
			<li><a href="#">My cruise</a></li>
			<li :class="{active: current == 'agents'}"><a href="#">Agents</a></li>
			<li><a href="#">Help</a></li>
		</ul>
	</div>
</template>

<script>
export default {
  data () {
    return {
      current: 'agents'
    }
  }
}
</script>

<style lang="stylus">
	@import "../assets/css/var";
	
	.tabs {
		display: flex;
		justify-content: space-between;
		position: relative;
		
		h3 {
			margin: 0px 20px;
			font-weight: bold;
			line-height: 40px;
			color: $dark;
		}

		ul {
			display: flex;
			justify-content: flex-end;
			margin-bottom: -2px;
			z-index: 2;
			
			li {
				margin: 0px 10px;
				display: inline-block;
				border: 2px solid $bd-color;
				padding: 10px 15px;
				border-radius: 5px 5px 0px 0px;
				
				a {
					text-decoration: none;
					color: $black;
				}

				&.active {
					border-bottom-color: $fill-color; 
					background-color: $fill-color;
					a {
						color: #fff;
					}
				}
			}
		}
	}
	/* Smartphones (portrait and landscape) ----------- */
	@media only screen and (min-device-width : 320px) and (max-device-width : 480px)
		.tabs	
			flex-direction: column
			ul
				flex-direction: column
</style>