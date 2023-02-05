<template>

  <button @click="button" class="w-33 h-11 col-span-2  border-2 rounded-lg flex  items-center text-xl font-bold sm:h-16 sm:w-33">{{big_button}}</button>

</template>

<script>
export default {
  props: {
    big_button: String,
    function: String,
  },

  methods : {
    button() {
      this.$emit('button')
    }
  }
}
</script>
