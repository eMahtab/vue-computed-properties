<template>
  <div class="hello">
    <h1>Message : {{ msg }}</h1>
    <h1>Reversed Message : {{ reversedMessage }}</h1>
    <button v-on:click="reverseIt">Reverse It</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  computed : {
    reversedMessage : function(){
      alert('Inside the reversedMessage computed getter ')
      return this.msg.split('').reverse().join('');
    }
  },
  methods : {
    reverseIt(){
      alert("Inside reverseIt method");
      this.msg = this.msg.split('').reverse().join('');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
