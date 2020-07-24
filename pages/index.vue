<template>
  <section class="container">
    <div>
      <h1 class="title">フルーツを選んでね</h1>
    </div>
    <div class="button-box">
      <a href="#" v-on:click="getFruit" class="button--grey">もも</a>
      <a href="#" v-on:click="getFruit" class="button--grey">りんご</a>
      <a href="#" v-on:click="getFruit" class="button--grey">すいか</a>
      <a href="#" v-on:click="getFruit" class="button--grey">みかん</a>
    </div>
    <div class="illust-box">
      <img v-bind:src="imgPath"/>
    </div>
  </section>
</template>

<script>
export default
{
  data: () => ({
    imgPath: ""
  }),

  methods: {
    getFruit() {
      this.imgPath = require('@/assets/peach.png');
    }
  }
}
</script>

<style>

.container {
  text-align:center;
  margin-top:10px;
}

.title{
  color:#4682b4;
}

.button-box{
  margin-top:30px;
}

.illust-box{
  margin-top:30px;
}

</style>