<template>
  <div id="app">
    <b-container class="bv-example-row">
      <b-row>
        <b-col md='4'>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sunt placeat aut tenetur in. Voluptas nobis iure     reprehenderit, iusto totam sequi?
        </b-col>
        <b-col md='4'>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sunt placeat aut tenetur in. Voluptas nobis iure     reprehenderit, iusto totam sequi?
        </b-col>
        <b-col md='4'>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sunt placeat aut tenetur in. Voluptas nobis iure     reprehenderit, iusto totam sequi?
        </b-col>
      </b-row>
      <hr>
      <b-row>
        <b-col md='4'>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse repellendus blanditiis tempore neque beatae accusamus deserunt magnam earum doloribus illo.
        </b-col>   
        <b-col md='4' offset-md='4'>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta ipsa enim eligendi dicta odio sed sequi facilis, obcaecati iste quasi.
        </b-col>
      </b-row>

      <b-row align-v="center" class="height">
        <b-col>Lorem ipsum dolor sit amet.</b-col>
        <b-col>Lorem ipsum dolor sit amet.</b-col>
        <b-col>Lorem ipsum dolor sit amet.</b-col>
      </b-row>

      <!-- Button -->
      <b-row align-v="center">
        <b-col cols="4">
          <b-button variant="danger" @click="handle">Button</b-button>
        </b-col>
        <b-col cols="4">
          <b-alert v-model="showDismissibleAlert" variant="danger" dismissible>
            Dismissible Alert!
          </b-alert>
        </b-col>
      </b-row>

      <b-row>
        <b-col>
          <b-button v-b-modal.das>Launch demo modal</b-button>

          <b-modal id="das" title="Sanu">
            <p class="my-4">Hello from modal!</p>
          </b-modal>
        </b-col>
      </b-row>

    </b-container>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      showDismissibleAlert: false
    }
  },
  methods: {
    handle: function() {
      this.showDismissibleAlert= true;
    }
  }
}
</script>

<style>
.height {
  min-height: 10rem;
  background: #444;
}
</style>
