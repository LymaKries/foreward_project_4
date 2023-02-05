<template>

  <button @click="button" class="w-11 h-11 border-2 rounded-lg text-center flex justify-center items-center text-white text-xl font-bold sm:h-16 sm:w-16">{{small_button}}</button>

</template>

<script>
export default {
  props: {
    small_button: String,
  },
  methods : {
    button() {
      this.$emit('button')
    }
  }
}
</script>
