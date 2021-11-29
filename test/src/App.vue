<template>
    <div id="app">
      <card></card>
      <ul>
        <li class="a" v-for="item in data" :key="item.name">
          <div>{{item}}</div>
        </li>
      </ul>
    </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Card from './components/Card.vue';

export default {
  data(){
    return{
      data:[],
    };
  },
  mounted(){
  this.axios.get('https://mocki.io/v1/5f533945-c82e-462e-92a4-b4e21490b560')
      .then((res)=>{
        console.log(res);
        this.data = res.data;
      })
  },
  name: 'App',
  components: {
    HelloWorld,
    Card
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
