<script>
  export default{
    data(){
      return{
        name: 'John Doe',
        status: 'pending',
        tasks: ['Task one', 'Task two', 'Task three'],
        link: 'https://www.google.com/'
      }
    },
    methods:{
      toggleStatus(){
        if(this.status === 'active')
      }
    }
  }
</script>
<template>
  <div class="flex">
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
 
    <h1>{{ name }}</h1>
    <p v-if="status === 'active'">User is active</p>
    <p v-else-if="status === 'pending'">User is pending</p>
    <p v-else>User is inactive</p>

    <h3>Tasks"</h3>
    <ul>
      <li v-for="task in tasks " :key="task">{{ task }}</li>
    </ul>
    <a v-bind:href="link" target="_blank">Go to google</a>

    <button v-on="click"></button>
  </div>


</template>Vue.js
<style scoped>
  h1{
    color: red;
  }
</style>