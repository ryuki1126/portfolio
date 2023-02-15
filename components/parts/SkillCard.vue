<template>
  <div class="card w-80 m-4 bg-base-100 shadow-xl">
  <figure class="h-40 px-10 pt-10">
    <img :src="this.skillData.imageLink" alt="skill" class="rounded-xl w-32" />
  </figure>
  <div class="card-body items-center text-center">
    <p class="text-xl">{{ this.skillData.span }}年経験しています</p>
    <p class="text-xl">自信は{{ this.skillData.confidence }}</p>
  </div>
</div>
</template>

<script>
export default {
  props: {
    skillData: {
      type: [
        Array,
        Object
      ]
    }
  }
}
</script>
