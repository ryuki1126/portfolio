<template>
<footer class="footer footer-center p-10 bg-base-200 text-base-content rounded">
  <div class="grid grid-flow-col gap-4">
    <a v-for="item in menuList" :key="item" :href="item.href" class="link link-hover hover:text-purple-500">{{ item.title }}</a> 
  </div> 
  <div>
    <div class="grid grid-flow-col gap-4">
      <a href="https://github.com/ryuki1126" target="_blank"><i class="text-4xl mdi mdi-github" /></a>
      <a href="https://github.com/ryuki1126" target="_blank"><i class="text-4xl mdi mdi-github" /></a>
      <a href="https://github.com/ryuki1126" target="_blank"><i class="text-4xl mdi mdi-github" /></a>
      <a href="https://github.com/ryuki1126" target="_blank"><i class="text-4xl mdi mdi-email" /></a>
    </div>
  </div> 
  <div>
    <p>Copyright © 2022 - All right reserved by ACME Industries Ltd</p>
  </div>
</footer>
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