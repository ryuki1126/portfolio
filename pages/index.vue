<template>
  <div class=" bg-slate-300">
    <Header 
      :menu-list='menuList'
    />
    <Top :id="menuList[0].id" />
    <div class="w-10/12 mx-auto bg-base-200 shadow-md">
      <About :id="menuList[1].id" />
      <Skills :id="menuList[2].id" />
      <Works :id="menuList[3].id" />
    </div>
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
    Skills: () => import('~/components/Skills'),
    Works: () => import('~/components/Works'),
    Footer: () => import('~/components/Footer'),
  },
  data() {
    return {
      menuList: [
        {
          title: 'Top',
          id: 'top',
          href: '#top'
        },
        {
          title: 'About Me',
          id: 'about',
          href: '#about'
        },
        {
          title: 'Skills',
          id: 'skills',
          href: '#skills'
        },
        {
          title: 'Works',
          id: 'works',
          href: '#works'
        }
      ]
    }
  }
}
</script>
