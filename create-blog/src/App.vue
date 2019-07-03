<template>
  <div>
    <app-header></app-header>
    <router-view></router-view>
  </div>
</template>

<script>
import addBlog from './components/addBlog';
import showBlogs from './components/showBlogs';
import listBlogs from './components/listBlogs';
import header from './components/header';

export default {
  components: {
    "add-blog": addBlog,
    "show-blog": showBlogs,
    "list-blog": listBlogs,
    "app-header": header
  },
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style>
body{
    margin: 0;
    font-family: 'Nunito SemiBold';
}
</style>
