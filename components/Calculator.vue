<template>
  <div class="w-full h-full bg-neutral-800 border-4 border-zinc-500 rounded">
    <div class="h-full flex flex-col justify-evenly content-evenly">
      <Title />

      <div class="w-full flex flex-col items-center">
        <div class="w-80 h-14 mb-3 bg-gray-200 border-2 border-zinc-500 rounded bottom-80"></div>

        <div class="w-80 h-96 bg-neutral-700 mb-3 border-4 border-zinc-400 rounded">
          <div class="grid grid-cols-4 grid-rows-5 gap-2 p-3">
            <BigButton @click="ac" class="bg-neutral-300 border-amber-500 text-neutral-400"
              big_button="AC"
            />

            <SmallButton class="bg-amber-500"
              small_button="="
            />

            <SmallButton class="bg-amber-500"
              small_button="%"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="7"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="8"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="9"
            />

            <SmallButton class="bg-amber-500"
              small_button="÷"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="4"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="5"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="6"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="X"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="1"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="2"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="3"
            />

            <SmallButton class="bg-amber-500"
              small_button="-"
            />

            <BigButton class="bg-neutral-400 border-neutral-300 bg-neutral-400 text-white"
              big_button="0"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
              small_button="."
            />

            <SmallButton class="bg-amber-500"
              small_button="+"
            />
          </div>
        </div>

      </div>

      <BottomText />
    </div>
  </div>
</template>


<script>

export default {
  data() {
    return {
      ac: "hey",
    };
  },
}
</script>

<script setup>
import BottomText from "./BottomText.vue";
import SmallButton from "./SmallButton.vue";
import BigButton from "./BigButton.vue";

</script>
