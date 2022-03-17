<template>
  <div>
    <Header 
      :menu-list='menuList'
    />
    <Top id="top" />
    <About id="about" />
    <Works id="works" />
    <Footer 
      :menu-list='menuList'
    />
  </div>
</template>

<script>
export default {
  components: {
    Header: () => import('~/components/Header'),
    Top: () => import('~/components/Top'),
    About: () => import('~/components/About'),
    Works: () => import('~/components/Works'),
    Footer: () => import('~/components/Footer'),
  },
  data() {
    return {
      menuList: [
        'About Me',
        'Skills',
        'Works'
      ]
    }
  }
}
</script>
