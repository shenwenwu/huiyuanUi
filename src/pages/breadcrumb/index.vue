<template>
  <div>
    <a href="https://github.com/aWestbrookFan/huiyuanUi/blob/master/src/pages/breadcrumb/index.vue" target="_blank">
      样例源码
    </a>
    <h6>
      基本用法:
    </h6>
    <f-breadcrumb
      :options="config.options"
    />

    <!--  -->
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
      title="options配置项"
      hide-bottom
      :tableData="config.optionsConfig.tableData"
      :columns="config.optionsConfig.columns"
    />
  </div>
</template>

<script>
import config from './config'
export default {
  name: 'pageBreadcrumb',
  data () {
    return {
      config
    }
  }
}
</script>

<style>
</style>
