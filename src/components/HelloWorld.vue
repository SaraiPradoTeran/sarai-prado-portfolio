<template>
  <div style="height: 97vh" class="center">
    <flipbook class="flipbook" :startPage="startPage" :pages="pages"></flipbook>
  </div>
</template>

<script>
import Flipbook from "flipbook-vue";

export default {
  components: { Flipbook },
  data() {
    return {
      startPage: null,
      pages: []
    };
  },
  mounted() {
    this.pages.push(null);
    for (let i = 1; i <= 58; i++) {
      this.pages.push(`./diapositivas/Diapositiva${i}.png`);
    }
  },
  name: "HelloWorld"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.flipbook {
  width: 90vw;
  height: 90vh;
}
.center {
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;

  -ms-flex-align: center;
  -webkit-align-items: center;
  -webkit-box-align: center;

  align-items: center;
}
</style>
