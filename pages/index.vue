<template>
  <section class="container">
    <div>
      <h1 class="title">フルーツを選んでね</h1>
    </div>
    <div class="button-box">
      <a href="#" v-on:click="getPeach" class="button--grey">もも</a>
      <a href="#" v-on:click="getApple" class="button--grey">りんご</a>
      <a href="#" v-on:click="getSuika" class="button--grey">すいか</a>
      <a href="#" v-on:click="getMikan" class="button--grey">みかん</a>
    </div>
    <div class="illust-box">
      <img v-bind:src="dispImg"/>
    </div>
  </section>
</template>

<script>
export default
{
  data: () => ({
    dispImg: ''
  }),

  methods: {
    getPeach() {
      this.dispImg = require('@/assets/peach.png');
    },
    getApple() {
      this.dispImg = require('@/assets/apple.png');
    },
    getSuika(){
      this.dispImg = require('@/assets/suika.png');
    },
    getMikan(){
      this.dispImg = require('@/assets/mikan.png');
    },
  }
}
</script>

<style>
.container {
  text-align:center;
  margin-top:10px;
}

.title{
  color:#FFC0CB;
}

.button-box,
.illust-box{
  margin-top:30px;
}

.button-box a{
  border-color:#FFA07A;
  color:#FFA07A;
}

.button-box a:hover{
  background-color: #FFA07A;
}
</style>