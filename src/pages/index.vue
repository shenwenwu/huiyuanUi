<template>
  <div>
<!--    <a target="_blank" href="https://github.com/darrenfei/f-vue-ui">github地址</a>-->

    <div class="f-coad-wrapper">
      <pre>
        // install

        npm install f-vue-ui

        // in main.js

        import FUI from 'f-vue-ui'

        // if you have install sass already

        impprt 'f-vue-ui/packages/css/style.scss'

        // else

        import 'f-vue-ui/packages/css/index.css'

        Vue.use(FUI)

        // example for input

        &lt;f-input v-model="inputValue"/&gt;
      </pre>
    </div>

    <div class="menu-mobile-wrapper">
      <h4 class="mt-sm mb-sm">
        菜单：
      </h4>
      <ul>
        <li
          v-for="(menu, idx) in menus"
          :key="'cmp_menu_' + idx"
          class="menu-item"
          :class="$route.path === menu.path ? 'text-primary' : ''"
          @click="_link(menu)"
        >
          <span class="menu-item-span inline-block full-width">{{ menu.name }}</span>
          <ul v-if="menu.children && menu.children.length > 0" class="pl-md mt-sm">
            <li
              v-for="(child, childIdx) in menu.children"
              :key="'cmp_menu_child_' + childIdx"
              class="menu-item-child"
              :class="$route.path === child.path ? 'text-primary' : ''"
              @click.stop="_link(child)"
            >
              {{ child.name }}
            </li>
          </ul>
        </li>
      </ul>
    </div>

  </div>
</template>

<script>
import menuData from '../components/menubar/menus.js'
export default {
  name: 'pageIndex',
  data () {
    return {
      menus: menuData
    }
  },
  methods: {
    _link (menu) {
      if (menu.path) {
        this.$router.push(menu.path)
      }
    }
  }
}
</script>

<style>

</style>
