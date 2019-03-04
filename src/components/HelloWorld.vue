<template>
  <div class="hello">
    <h3>Data inside of a string <br />item.url: {{ item.url }}</h3>
    <a :href="item.url">Data bound to href attribute</a>
    <h5>Data bound to image src attribute</h5>
    <hr />
    <img :src="item.url" /> <img :src="item.tyler" />
    <hr />
    <p>
      Want to change the data?<br />Use v-model to bind an input to some
      data.<br />(try changing 300 to 310)
    </p>
    <input type="text" v-model="item.url" />
  </div>
</template>

<script>
import tylerImage from "@/assets/tyler.png";

export default {
  name: "HelloWorld",
  data() {
    return {
      item: {
        url: "https://www.placecage.com/gif/200/300",
        tyler: tylerImage
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input {
  width: 50%;
  text-align: center;
}
</style>
