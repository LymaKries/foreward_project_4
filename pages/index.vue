<template>
  <div class="w-screen h-screen p-3">
    <div class="h-full flex flex-col">
      <Title />
      <Calculator />
    </div>
  </div>
</template>

<script>
import Calculator from "../components/Calculator.vue";
import Title from "../components/Title.vue";

export default {
  name: 'IndexPage',
  components: {Title, Calculator}
}
</script>
