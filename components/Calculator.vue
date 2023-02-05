<template>
  <div class="w-full h-full bg-neutral-800 border-4 border-zinc-500 rounded">
    <div class="h-full flex flex-col justify-evenly content-evenly">
      <Title />

      <div class="w-full flex flex-col items-center ">
        <div class="w-56 h-10 pr-1 mb-3 bg-gray-200 border-2 border-zinc-500 rounded bottom-80 text-3xl flex items-center justify-end sm:w-80 sm:h-14 sm:te">{{input}}</div>

        <div class="w-56 h-80 bg-neutral-700 mb-3 border-4 border-zinc-400 rounded-lg sm:w-80 sm:h-96">
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
                         small_button="x"
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


<script setup>

import BottomText from "./BottomText.vue";
import SmallButton from "./SmallButton.vue";
import BigButton from "./BigButton.vue";
</script>

<script>
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
    },

    zero() {
      if (this.operation === "") {
        this.operation = 0;
        this.result = 0;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 0;
          this.operation += "0";
          this.result += 0;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 0;
          this.operation += "0";
          this.result -= 0;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 0;
          this.operation += "0";
          this.result /= 0;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 0;
          this.operation += "0";
          this.result *= 0;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 0;
          this.operation += "0";
          this.result *= 0;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "0";
          this.operation += "0";
          this.result += 0.0;
          return;
        }
      }
      this.input = 0;
    },

    one() {

      if (this.operation === "") {
        this.input = 1;
        this.operation = 1;
        this.result = 1;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+") {
          this.input = 1;
          this.operation += "1";
          this.result += 1;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 1;
          this.operation += "1";
          this.result -= 1;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 1;
          this.operation += "1";
          this.result /= 1;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 1;
          this.operation += "1";
          this.result *= 1;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "1";
          this.operation += "1";
          this.result += 0.1;
          return;
        }
      }
      this.input = 1;
    },

    two() {
      console.log(this.input);

      if (this.operation === "") {
        this.operation = 2;
        this.result = 2;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 2;
          this.operation += "2";
          this.result += 2;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 2;
          this.operation += "2";
          this.result -= 2;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 2;
          this.operation += "2";
          this.result /= 2;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 2;
          this.operation += "2";
          this.result *= 2;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "2";
          this.operation += "2";
          this.result += 0.2;
          console.log(this.result);
          return;
        }
      }
      this.input = 2;
    },

    three() {
      if (this.operation === "") {
        this.operation = 3;
        this.result = 3;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 3;
          this.operation += "3";
          this.result += 3;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 3;
          this.operation += "3";
          this.result -= 3;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 3;
          this.operation += "3";
          this.result /= 3;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 3;
          this.operation += "3";
          this.result *= 3;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "3";
          this.operation += "3";
          this.result += 0.3;
          return;
        }
      }
      this.input = 3;
    },

    four() {
      if (this.operation === "") {
        this.operation = 4;
        this.result = 4;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 4;
          this.operation += "4";
          this.result += 4;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 4;
          this.operation += "4";
          this.result -= 4;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 4;
          this.operation += "4";
          this.result /= 4;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 4;
          this.operation += "4";
          this.result *= 4;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "4";
          this.operation += "4";
          this.result += 0.4;
          return;
        }
      }
      this.input = 4;
    },

    five() {
      if (this.operation === "") {
        this.operation = 5;
        this.result = 5;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 5;
          this.operation += "5";
          this.result += 5;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 5;
          this.operation += "5";
          this.result -= 5;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 5;
          this.operation += "5";
          this.result /= 5;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 5;
          this.operation += "5";
          this.result *= 5;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "5";
          this.operation += "5";
          this.result += 0.5;
          return;
        }
      }
      this.input = 5;
    },

    six() {
      if (this.operation === "") {
        this.operation = 6;
        this.result = 6;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 6;
          this.operation += "6";
          this.result += 6;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 6;
          this.operation += "6";
          this.result -= 6;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 6;
          this.operation += "6";
          this.result /= 6;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 6;
          this.operation += "6";
          this.result *= 6;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "6";
          this.operation += "6";
          this.result += 0.6;
          return;
        }
      }
      this.input = 6;
    },

    seven() {
      if (this.operation === "") {
        this.operation = 7;
        this.result = 7;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 7;
          this.operation += "7";
          this.result += 7;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 7;
          this.operation += "7";
          this.result -= 7;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 7;
          this.operation += "7";
          this.result /= 7;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 7;
          this.operation += "7";
          this.result *= 7;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "7";
          this.operation += "7";
          this.result += 0.7;
          return;
        }
      }
      this.input = 7;
    },

    eight() {
      if (this.operation === "") {
        this.operation = 8;
        this.result = 8;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 8;
          this.operation += "8";
          this.result += 8;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 8;
          this.operation += "8";
          this.result -= 8;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 8;
          this.operation += "8";
          this.result /= 8;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 8;
          this.operation += "8";
          this.result *= 8;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "8";
          this.operation += "8";
          this.result += 0.8;
          return;
        }
      }
      this.input = 8;
    },

    nine() {
      if (this.operation === "") {
        this.operation = 9;
        this.result = 9;
      }

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "+"){
          this.input = 9;
          this.operation += "9";
          this.result += 9;
          return;
        }

        if (this.operation[i] === "-") {
          this.input = 9;
          this.operation += "9";
          this.result -= 9;
          return;
        }

        if (this.operation[i] === "/") {
          this.input = 9;
          this.operation += "9";
          this.result /= 9;
          return;
        }

        if (this.operation[i] === "*") {
          this.input = 9;
          this.operation += "9";
          this.result *= 9;
          return;
        }

        if (this.operation[i] === ".") {
          this.input += "9";
          this.operation += "9";
          this.result += 0.9;
          return;
        }
      }
      this.input = 9;
    },

    addition() {
      if (this.operation === "") {
        this.operation = "0+";
      }

      this.operation += "+";
    },

    division() {
      if (this.operation === "") {
        this.operation = "0/";
      }

      this.operation += "/";
    },

    multiplication() {
      if (this.operation === "") {
        this.operation = "0*";
      }

      this.operation += "*";
    },

    soustraction() {
      if (this.operation === "") {
        this.operation = "0-";
      }

      this.operation += "-";
    },

    modulo() {
      // if (this.operation === "") {
      //   this.operation = "0%";
      // }
      //
      // this.operation += "%";
      this.input= "it doesn't work, sorry"
    },

    res() {

      for (var i = 0; i < this.operation.length; i++) {
        if (this.operation[i] === "/0"){
          this.input = "error"
        }
        this.input = this.result;
      }
    },

    decimal() {
      if (this.operation === "") {
        this.operation = "0.";
      } else {
        this.operation += ".";
      }
      this.input += ".";
    }
  },
}

</script>
