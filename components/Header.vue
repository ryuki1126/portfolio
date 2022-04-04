<template>
  <div class="navbar bg-neutral text-green-400 fixed z-10">
  <div class="flex-1">
    <a href="#top" class="btn btn-ghost normal-case text-xl ">Ryuki's Portfolio</a>
  </div>
  <div class="flex-none">
    <ul class="menu menu-horizontal p-0 mr-4 text-white">
      <li tabindex="0">
        <a>
          menu
          <svg class="fill-current" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z"/></svg>
        </a>
        <ul class="p-2 bg-neutral">
          <li v-for="item in menuList" :key="item" class="hover:text-purple-400"><a :href="item.href">{{ item.title }}</a></li>
        </ul>
      </li>
    </ul>
  </div>
</div>
</template>

<script>
export default {
  props: {
    menuList: {
      type: [
        Array,
        Object
      ]
    }
  }
}
</script>