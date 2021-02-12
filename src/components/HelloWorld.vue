<template>
  <div class="hello">
    <p>Práctica de Vue.</p>
    <br>
    <button v-on:click="count">Haz click aquí.</button>
    <input v-model="contador" placeholder="count" readonly>
    <br>
    <span>{{ mensaje }}</span>
    <button @click="destroy()">Destroy</button>

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
      contador:0,
      mensaje:'El siguiente botón "mata" la página y muestra beforeDestroyed y destoyed en consola.'
    };

},
  methods:{
    count(){
      this.contador+=1;
    },
    destroy(){
      this.$destroy();
    }
  },
  beforeCreate() {
    console.log('beforeCreate')
  },
  created() {
    console.log('created')
  },
  beforeMount() {
    console.log('beforeMount')
  },
  mounted() {
    console.log('mounted')
  },
  beforeUpdate() {
    console.log('beforeUpdate')
  },
  updated() {
    console.log('updated')
  },
  beforeDestroy() {
    console.log('beforeDestroy')
  },
  destroyed() {
    console.log('destroyed')
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
button{
  margin: 15px;
}
</style>
