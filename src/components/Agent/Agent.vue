<template>
    <div class="agents">
        <filter></filter>
        <div class="agent-container">
            <div class="list box">
                <div v-for="agent in agents">
                    <item :agent="agent"></item>
                </div >
            </div>
            <div class="detail box">
                <detail></detail>
            </div>
        </div>
    </div>
</template>
<script>
import Item from './Item'
import Filter from './Filter'
import Detail from './Detail'
import agents from './agents.json'

export default {
  data () {
    return {
      agents: agents
    }
  },
  components: {
    Item,
    Filter,
    Detail
  }
}
</script>

<style lang="stylus">
    @import '../../assets/css/var'
    
    .agents {
        display: flex;
        position: relative;
        width: 100%;
        border: 2px solid $bd-color;
        flex-direction: column;
        
        .agent-container {
            display: flex;
            width: 100%;
        }
        
        .filter {
            height: 50px;
            width: 100%;
            background-color: $fill-color;
        }

        .box {
            padding: 0px 20px;
            display: flex;
        }
        
        .list {
            flex: 6;
            flex-direction: column;
            margin-bottom: 20px;
        }
        
        .detail {
            flex: 2;
            height: auto;
            border-left: 2px solid $bd-color;
        }
    }
</style>