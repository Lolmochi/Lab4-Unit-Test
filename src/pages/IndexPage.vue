<template>
  <div class="htmlClass">
    <h1>{{ title }}</h1>
    <form>
      <input type="text" id="firstValue"  v-model="firstValue" />
      <input type="text" id="secondValue" v-model="secondValue" />
      <input type="text" id="answerVulue" v-model="answerVulue" />
      <input type="text" id="fistname"    v-model="fistname" />
      <input type="text" id="lastname"    v-model="lastname" />
      <input type="text" id="id"          v-model="id" />
      <button @click="addition(firstValue,secondValue)" >Addition</button>
      <button @click="subtraction(firstValue,secondValue)" >Subtraction</button>
      <button @click="multiplication(firstValue,secondValue)" >Multiplication</button>
      <button @click="divide(firstValue,secondValue)" >Divide</button>
  </form>
  </div>
</template>
<script>

export default {
  name: 'HtmlComponent',
  data() {
    return {
      title: 'Vue is awesome.',
      firstValue:0,
      secondValue:0,
      answerVulue:0,
      fistname:"Adison",
      lastname:"Wongkham",
      id:"6404101350"
    }
  },
  methods: {
    // https://jestjs.io/docs/using-matchers
    // https://www.philbarresi.com/jest-test-guide/
    addition(first, second) {
      this.answerVulue =  Number(first) + Number(second)
      return this.answerVulue;
    },
    subtraction(first, second ) {
      this.answerVulue =  Number(first) - Number(second)
      return this.answerVulue;
    },
    multiplication(first, second ) {
      this.answerVulue =  Number(first) * Number(second)
      return this.answerVulue;
    },
    divide(first, second) {
      this.answerVulue =  Number(first) / Number(second)
      return this.answerVulue;
    },
  },
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>