<template>
  <div>
    <a href="https://github.com/aWestbrookFan/huiyuanUi/blob/master/packages/css/style.scss" target="_blank">
      样例源码
    </a>
    <f-table
      class="mt-md"
      title="配置项详解"
      hide-bottom
      :tableData="config.cssConfig.tableData"
      :columns="config.cssConfig.columns"
    />
  </div>
</template>

<script>
import config from './config'
export default {
  name: 'pageCss',
  data () {
    return {
      config
    }
  }
}
</script>

<style>
</style>
