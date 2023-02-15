<template>
  <div class="card card-side bg-base-100 shadow-xl m-3">
    <figure><img :src="this.workData.imageLink" alt="work" class="w-40"></figure>
    <div class="card-body">
      <h2 class="card-title">{{ this.workData.name }}</h2>
      <p>{{ this.workData.overview }}</p>
      <div class="mt-8 card-actions justify-end">
        <!-- The button to open modal -->
        <label :for="this.workData.name" class="btn modal-button hover:text-purple-500">詳しく！</label>

        <!-- Put this part before </body> tag -->
        <input type="checkbox" :id="this.workData.name" class="modal-toggle">
        <label :for="this.workData.name" class="modal cursor-pointer">
          <label class="modal-box relative" for="">
            <h3 class="text-xl font-bold">{{ this.workData.name }}</h3>
            <p>{{ this.workData.overview }}</p>
            <div class="my-8">
              <p class="text-lg font-bold">機能</p>
              <ul class="pl-4">
                <li v-for="feature in this.workData.features" :key="feature" class="list-disc">{{ feature }}</li>
              </ul>
            </div>
            <div class="my-8">
              <p class="text-lg font-bold">使用技術</p>
              <ul class="pl-4">
                <li v-for="skill in this.workData.skills" :key="skill" class="list-disc">{{ skill }}</li>
              </ul>
            </div>
            <div class="my-8">
              <p class="text-lg font-bold">学び</p>
              <p>{{ this.workData.knowledge }}</p>
            </div>
            <div class="my-8">
              <p class="text-lg font-bold">外部リンク</p>
              <a v-if="this.workData.github !== null" :href="this.workData.github" target="_blank"><i class="text-4xl mdi mdi-github" /></a>
              <a v-if="this.workData.siteLink !== null" :href="this.workData.siteLink" target="_blank"><i class="text-4xl mdi mdi-application-outline ml-2" /></a>
              <p v-if="this.workData.github === null">機密のため公開できません🙇‍♂️</p>
            </div>
          </label>
        </label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    workData: {
      type: [
        Array,
        Object
      ]
    }
  }
}
</script>