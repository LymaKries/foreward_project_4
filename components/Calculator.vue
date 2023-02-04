<template>
  <div class="w-full h-full bg-neutral-800 border-4 border-zinc-500 rounded">
    <div class="h-full flex flex-col justify-evenly content-evenly">
      <Title />

      <div class="w-full flex flex-col items-center ">
        <div class="w-80 h-14 pr-1 mb-3 bg-gray-200 border-2 border-zinc-500 rounded bottom-80 text-3xl flex items-center justify-end">{{input}}</div>

        <div class="w-80 h-96 bg-neutral-700 mb-3 border-4 border-zinc-400 rounded-lg">
          <div class="grid grid-cols-4 grid-rows-5 gap-2 p-3">
            <BigButton class="bg-neutral-300 border-amber-500 text-neutral-400 pl-3"
                       big_button="AC"
                       @button="ac"
            />

            <SmallButton class="bg-amber-500 border-amber-500 border-slate-500"
                         small_button="="
                         @button="res"
            />

            <SmallButton class="bg-amber-500 border-slate-500"
                         small_button="%"
                         @button="modulo"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="7"
                         @button="seven"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="8"
                         @button="eight"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="9"
                         @button="nine"
            />

            <SmallButton class="bg-amber-500 border-slate-500"
                         small_button="÷"
                         @button="division"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="4"
                         @button="four"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="5"
                         @button="five"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="6"
                         @button="six"
            />

            <SmallButton class="bg-amber-500 border-slate-500"
                         small_button="X"
                         @button="multiplication"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="1"
                         @button="one"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="2"
                         @button="two"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="3"
                         @button="three"
            />

            <SmallButton class="bg-amber-500 border-slate-500"
                         small_button="-"
                         @button="soustraction"
            />

            <BigButton class="bg-neutral-400 border-neutral-300 bg-neutral-400 text-white justify-center"
                       big_button="0"
                       @button="zero"
            />

            <SmallButton class="border-neutral-300 bg-neutral-400"
                         small_button="."
                         @button="decimal"
            />

            <SmallButton class="bg-amber-500 border-slate-500"
                         small_button="+"
                         @button="addition"
            />
          </div>
        </div>

      </div>

      <BottomText />
    </div>
  </div>
</template>


<script>

import BottomText from "./BottomText.vue";
import SmallButton from "./SmallButton.vue";
import BigButton from "./BigButton.vue";

export default {
  data() {
    return {
      input: 0,
      operation: "",
      result:0,
    };
  },
  methods : {
    ac() {
      this.operation = "";
      this.result = 0;
      this.input = 0;
      console.log(this.result)
      console.log(this.operation)

    },

    one() {
      this.input = 1;

      if (this.operation === "") {
        this.input = 1;
        this.operation = 1;
        this.result = 1;
        console.log('vide')
        console.log(this.operation)
        console.log(this.result)
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 1;
          this.operation += "1";
          this.result += 1;
          console.log('ya un +')
          console.log(this.operation)
          console.log(this.result)
          return;
        }

      }
    },

    two() {
      this.input = 2;

      if (this.operation === "") {
        this.operation = 2;
        this.result = 2;
        console.log(this.operation)
        console.log(this.result)
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 2;
          this.operation += "2";
          this.result += 2;
          console.log('ya un +')
          console.log(this.operation)
          console.log(this.result)
          return;
        }

        // if (this.operation.length > 0 && this.operation.lenght-1 !== "+"){
        //     this.input += 2;
        //     this.operation += "2";
        //     this.result += 2;
        //     console.log('rajoute chiffre')
        //     console.log(this.operation)
        //     console.log(this.result)
        //     return;
        // }
      }
    },

    addition() {
      if (this.operation === "") {
        this.operation = "0+";
      }

      this.operation += "+";

      console.log(this.result)
      console.log(this.operation)
    },

    res() {
      this.input = this.result;
      console.log(this.result)
      console.log(this.operation)
    },

    // addition() {
    //   this.operation
    // }
    },
}

</script>
