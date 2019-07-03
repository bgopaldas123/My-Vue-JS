<template>
  <div id="show-blogs">
    <h1>All Blog Articles</h1>
    <input type="text" v-model="search" placeholder="search blogs">
    <div v-for="(blog, index) in filteredBlogs" v-bind:key="index" class="single-blog">
      <router-link v-bind:to="'/blog/' + blog.id"><h2 v-rainbow>{{ blog.title | to-uppercase }}</h2></router-link>
      <article>{{ blog.body | snippet }}</article>
    </div>
  </div>
</template>

<script>
import searchMixins from "../mixins/searchMixins";

export default {
  
  data () {
    return {
      blogs: [],
      search: ''
    }
  },
  created () {
    this.$http.get('https://jsonplaceholder.typicode.com/posts').then((data) => {
      console.log(data);
      this.blogs = data.body.slice(0, 10);
    })
  },
  computed: {
    
  },
  filters: {
    "to-uppercase": function(value) {
      return value.toUpperCase();
    }
  },
  directives: {
    "rainbow": {
      bind(el, binding, vnode) {
        el.style.color = "#" + Math.random().toString().slice(2, 8);        
      }
    }
  },
  mixins: [searchMixins]
}
</script>

<style>
#show-blogs{
    max-width: 800px;
    margin: 0px auto;
}
.single-blog{
    padding: 20px;
    margin: 20px 0;
    box-sizing: border-box;
    background: #eee;
}
</style>
