<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <h3>Handling user input</h3>
    <p>{{ msgR }}</p>
    <button v-on="reverse">Reverse Message</button>


  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      msgR: "Hello reverse"
    }
  },
  methods: {
    reverse(){
      this.msgR = this.msgR.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
