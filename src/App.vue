<template>
  <div id="app">
    <top></top>
    <tabs></tabs>
    <agent></agent>
  </div>
</template>

<script>
require('./assets/css/reset.css')
import * as Top from './components/Header'
import Tabs from './components/Tabs'
import { Agent } from './components/Agent'

export default {
  components: {
    Top,
    Tabs,
    Agent
  }
}
</script>

<style>
html, body, #app {
  height: 100%;
}

#app {
  color: #2c3e50;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
  margin: 0px 20px;
}
</style>
