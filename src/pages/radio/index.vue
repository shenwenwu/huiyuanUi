<template>
  <div>
    <a href="https://github.com/aWestbrookFan/huiyuanUi/blob/master/src/pages/radio/index.vue" target="_blank">
      样例源码
    </a>
    <h6>基本用法：</h6>
    <f-radio v-model="radioModel" val="test1" label="test1"/>
    <f-radio v-model="radioModel" val="test2" label="test2"/>
    <f-radio v-model="radioModel" val="test3" label="test3"/>

    <f-table
      class="mt-md"
      title="配置项详解"
      hide-bottom
      :tableData="config.settingConfig.tableData"
      :columns="config.settingConfig.columns"
    />

    <!--  -->
    <f-table
      class="mt-md"
      title="emit"
      hide-bottom
      :tableData="config.emitConfig.tableData"
      :columns="config.emitConfig.columns"
    />
  </div>
</template>

<script>
import config from './config'
export default {
  name: 'pageRadio',
  data () {
    return {
      config,
      radioModel: ''
    }
  }
}
</script>

<style>

</style>
