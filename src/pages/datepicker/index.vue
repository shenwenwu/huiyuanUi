<template>
  <div>
<!--    <a href="https://github.com/aWestbrookFan/huiyuanUi/blob/master/src/pages/datepicker/index.vue" target="_blank">-->
<!--      样例源码-->
<!--    </a>-->
    <h6>
      基本用法:
    </h6>

    <f-datepicker v-model="date"/>

    <h6>
      format="YYYY/MM/DD"
    </h6>
    <f-datepicker
      format="YYYY/MM/DD"
    />

    <h6>
      disabled
    </h6>
    <f-datepicker
      disabled
    />

    <h6>
      border="underline"
    </h6>
    <f-datepicker
      border="underline"
    />

    <h6>
      min（前10天）
    </h6>
    <f-datepicker
      :min="min"
    />

    <h6>
      max（后十天）
    </h6>
    <f-datepicker
      :max="max"
    />

    <h6>
      min & max （前10天到后十天）
    </h6>
    <f-datepicker
      :min="min"
      :max="max"
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
      title="emit"
      hide-bottom
      :tableData="config.emitConfig.tableData"
      :columns="config.emitConfig.columns"
    />
  </div>
</template>

<script>
  import config from './config'
  import {date} from '../../../packages/utils/date'

  export default {
    name: 'pageDatepicker',
    data() {
      return {
        config,
        date: new Date(Date.now()),
        min: date.getPrevDate(new Date(), 10),
        max: date.getNextDate(new Date(), 10)
      }
    }
  }
</script>

<style>
</style>
