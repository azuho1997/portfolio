<template>
  <div class="color">
    <div class="bg"></div>
    <div class="title">AZUHO'S PORTFOLIO</div>
    <div>
      <!-- <div class="bg"></div> -->
      <router-link to="/next">
        <button class="button">OPEN</button>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
    mounted () {
    setTimeout(this.$router.push("next"), 3000);
    },
    transition: "test",
    methods: {}
};
</script>

<style scoped>
.button {
  animation: flashing 2s ease-out;
  animation-iteration-count: infinite; /*繰り返し回*/
  font-size: 1.4em;
  font-weight: bold;
  padding: 10px 30px;
  -moz-border-radius: 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  left: 45%;
  top: 60%;
  text-align: center;
  letter-spacing: 0.2em;
  transition: opacity 0.24s ease-in;
  width: 10%;
  height: 2.2em;
  position: absolute;
  transition: width 2s;
}

.button:hover {
  opacity: 0.5;
  width: 20%;
}

.title {
  font-size: 180%;
  border-bottom: solid 20px rgb(155, 118, 149);
  text-align: center;
  padding: 17%;
  letter-spacing: 0.9em;
  font-weight: 800;
  width: 100%;
  height: 45%;
  position: absolute;
}

.bg {
  /*位置の設定*/
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;

  /*背景画像の設定*/
  background-image: url("~@/assets/ver2.jpg");
  background-size: cover;

  /*透過の設定*/
  opacity: 0.5;
}
</style>
