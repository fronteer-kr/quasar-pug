<template lang="pug">
q-page.q-gutter-y-md(padding)
  .text-h4 About

  div
    .text-h5 Font 확인
    p
      | 먹이를 찾아 산기슭을 어슬렁거리는
      | 하이에나를 본 일이 있는가
      | 짐승의 썩은 고기만을 찾아다니는
      | 산기슭의 하이에나
      | 나는 하이에나가 아니라 표범이고 싶다
      | 산정 높이 올라가 굶어서 얼어 죽는
      | 눈 덮인 킬리만자로의 그 표범이고 싶다

  div
    .text-h5 Components 확인
    q-date(v-model="dateA")


</template>

<script setup>
import { ref } from "vue";

const dateA = ref("2022/10/25");
</script>

<style lang="scss" scoped></style>
