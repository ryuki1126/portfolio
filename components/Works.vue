<template>
    <div class="pt-16 pb-40">
    <h3 class="text-center dark:text-white text-3xl font-bold">WORKS</h3>
    <div class="w-20 h-1 mt-2 mx-auto bg-green-500"></div>
    <div class="pt-32 flex justify-center flex-wrap">
      <WorkCard v-for="work in works" :key="work.name" :workData="work" />
    </div>
  </div>
</template>

<script>
export default {
  components: {
    WorkCard: () => import('~/components/parts/WorkCard.vue'),
  },
  data() {
    return {
      works: [
        {
          name: '廃油管理アプリ',
          overview: 'RFタグを活用して廃油タンク数を管理するIoTアプリ',
          skills: [
            'Nuxt.js',
            'Express(Node.js)',
            'AWS(EC2,RDS)',
            'mysql',
            'nginx'
          ],
          features: [
            'マイコンから送信されるデータをDBに登録する機能',
            '廃油の数が基準値を超えたらメール通知する機能',
            'JWTによる認証機能',
            'chartjsライブラリを利用したグラフによるデータの可視化'
          ],
          knowledge: 'グラフ描画をリアクティブにする実装で沼りました。状態管理やエラー耐性、認証機能など、基本的な技術を身につけました。また、このアプリの開発で初めてAWSを利用したので、インフラの知識が身につきました。',
          github: null,
          imageLink: require('~/assets/image/nuxtjs.png')
        },
        {
          name: 'バッテリーBMS管理用API',
          overview: 'バッテリーの電圧や温度等のデータを受信するAPI',
          skills: [
            'Express(Node.js)',
            'AWS(EC2,RDS)',
            'mysql',
            'nginx'
          ],
          features: [
            'マイコンから送信されるデータをDBに登録する機能',
            'バッテリー容量が30％以下の場合メール通知する機能',
            'エラー信号がTRUEの場合メール通知する機能',
            '10分おきの通信が滞っている場合メール通知する機能'
          ],
          knowledge: '簡単なDB構造ではありますが、リレーションを意識したDB構築を学びました。',
          github: 'https://github.com/ryuki1126/bms_api',
          imageLink: require('~/assets/image/nodejs.jpg')
        },
        {
          name: 'Next.js学習時に作成したブログサイト',
          overview: 'Next.jsに触れてみたくて作ったマイクロブログ',
          skills: [
            'Next.js',
            'Vercel'
          ],
          features: [
            '特にありません🙇‍♂️'
          ],
          knowledge: 'Next.js製のアプリをVercelでデプロイする便利さを知りました…！',
          github: 'https://github.com/ryuki1126/next.js-microblog',
          imageLink: require('~/assets/image/nextjs.png')
        },
      ]
    }
  }
}
</script>
