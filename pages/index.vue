<template>
  <div>
    <Header />
    <Top />
    <div class="w-10/12 mx-auto">
      <h1>hello</h1>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  components: {
    Header: () => import('~/components/Header'),
    Top: () => import('~/components/Top'),
    Footer: () => import('~/components/Footer'),
  },
}
</script>
