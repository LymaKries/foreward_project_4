<template>

  <button @click="button" class="col-span-2 h-16 w-33 border-2 rounded-lg flex  items-center text-xl font-bold">{{big_button}}</button>

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
