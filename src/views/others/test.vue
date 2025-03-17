<template>
  <operate-box>
    <el-button @click="test1" type="primary">test1</el-button>
    <el-button @click="test2" type="primary">test2</el-button>
  </operate-box>
</template>
<script setup>
import { ref } from 'vue'
import * as Cesium from 'cesium'
const test1 = () => {
  console.log('test1')
}
const test2 = () => {
  console.log('test2')
}

const { viewer } = window

let czmldata = new Cesium.CzmlDataSource.load('/models/wx.czml');
viewer.dataSources.add(czmldata)
viewer.clock.shouldAnimate = true;
</script>
<style lang='less' scoped></style>