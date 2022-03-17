<template>
  <div>
    <Header />
    <Top />
    <div class="w-10/12 mx-auto">
      <About />
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  components: {
    Header: () => import('~/components/Header'),
    Top: () => import('~/components/Top'),
    About: () => import('~/components/About'),
    Footer: () => import('~/components/Footer'),
  },
}
</script>
