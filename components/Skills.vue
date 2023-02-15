<template>
  <div class="pt-16 pb-40">
    <h3 class="text-center dark:text-white text-3xl font-bold">SKILLS</h3>
    <div class="w-20 h-1 mt-2 mx-auto bg-green-500"></div>
    <div class="pt-32 flex justify-center">
      <div class="w-4/5">
        <div class="flex justify-center flex-wrap">
          <SkillCard v-for="skill in skills" :key="skill.name" :skillData="skill" />
        </div>
        <div class="pt-20 pl-20 text-sm">
          <p>自信についてはあくまで自信です。実力との乖離がある可能性がございます💦<br>予めご了承ください🙇‍♂️</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {
    SkillCard: () => import('~/components/parts/SkillCard.vue'),
  },
  data() {
    return {
      skills: [
        {
          name: 'node.js',
          span: '2',
          confidence: '凄くあります！',
          imageLink: require('~/assets/image/nodejs.jpg')
        },
        {
          name: 'nuxt.js',
          span: '1',
          confidence: 'あります！',
          imageLink: require('~/assets/image/nuxtjs.png')
        },
        {
          name: 'nextjs',
          span: '0.5',
          confidence: 'ちょっとあります…！',
          imageLink: require('~/assets/image/nextjs.png')
        },
        {
          name: 'php',
          span: '1',
          confidence: 'あります！',
          imageLink: require('~/assets/image/php.png')
        },
        {
          name: 'python',
          span: '2',
          confidence: 'あります！',
          imageLink: require('~/assets/image/python.png')
        },
        {
          name: 'aws',
          span: '1',
          confidence: 'ちょっとあります…！',
          imageLink: require('~/assets/image/aws.jpeg')
        },
      ]
    }
  }
}
</script>
