<template>
  <div class="w-screen h-screen p-3">
    <div class="h-full flex flex-col">
      <HeadTitle />
      <Calculator />
    </div>
  </div>
</template>

<script>
import Calculator from "../components/Calculator.vue";
import HeadTitle from "../components/HeadTitle.vue";

export default {
  name: 'IndexPage',
  components: {HeadTitle, Calculator}
}
</script>
