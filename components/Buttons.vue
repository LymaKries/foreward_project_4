<template>

  <div>
    <div class="bg-black h-5 w-5">{{big_button1}}</div>

    <div class="bg-rose-800 h-5 w-5">{{grey_button}}</div>

    <div class="bg-white h-5 w-5">{{orange_button}}</div>

    <div class="bg-blue-200 h-5 w-5">{{big_button2}}</div>
  </div>

</template>

<script>
export default {
  props: {
    big_button1: String,
    grey_button: String,
    orange_button: String,
    big_button2: String
  },
}
</script>
