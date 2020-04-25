<template>
  <div>
    <div>
    <nav class="navbar navbar-expand-lg scrolling-navbar navbar-light bg-light fixed-top">
      <div class="navbar-brand row">
        <div class="col-md-12 col-12">
          <span >
            <img src="https://d3i4yxtzktqr9n.cloudfront.net/web-eats-v2/ee037401cb5d31b23cf780808ee4ec1f.svg">
          </span>
          <!-- <span class="col-md-1 col-1">
            Sign In
          </span> -->
        </div>
      </div>
    </nav>
    </div>

    <HelloWorld msg="Welcome to Your Vue.js App"/>
       <div class="bg-dark text-light">
      <br><br>
      <div class="container">
        <div class="col-md-12 row">
          <div class="col-md-6">
            <img src="https://d3i4yxtzktqr9n.cloudfront.net/web-eats-v2/c266ad32e5e88af804b3a1b6b60098f9.svg">
          </div>
          
          <div class="col-md-3"><br>
            <div :key="level" v-for="level in col2">
              <div>
                {{level}}
              </div><br>
            </div>
          </div>

          <div class="col-md-3"><br>
           <div :key="level" v-for="level in col3">
              <div>
                {{level}}
              </div><br>
            </div>
           </div>
        </div>
        
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return{
      col2:[],
      col3:[]
    }
  },
  created(){
    this.col2 = [
      'Read our blog',
      'Create a business account',
      'About Uber Eats',
      'Buy gift cards',
      'Add your restaurant',
      'Sign up to deliver'
    ];
    this.col3 = [
      'Get Help',
      'Read FAQs',
      'View all cities',
      'View all countries',
      'Restaurants near me',
      'English'
    ]
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
