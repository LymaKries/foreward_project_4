<template>

  <button class="h-16 w-16 border-2 rounded text-center flex justify-center items-center text-white text-xl font-bold">{{small_button}}</button>

</template>

<script>
export default {
  props: {
    small_button: String,
  },
}
</script>
