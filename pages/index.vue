<template>
  <div class="color">
    <div class="bg"></div>
      <div class="title">
    <span v-for="(t, index) in text" :key="index" class="item" :style="{animationDelay: index*100+'ms'}" v-text="t"/>          
      </div>
    <div class="container">
      <router-link to="/next" class="button">
        OPEN
      </router-link>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      text: "AZUHO'S PORTFOLIO"
    }
  }
}
</script>

<style scoped>
@keyframes text-in {
  0% {
    transform: translate(0, -20px);
    opacity: 0;
  }
}
.item {
  color: #FFF;
  -webkit-text-stroke: 3px rgb(126, 190, 190);
  display: inline-block;
  min-width: 0.3em;
  font-size: 2rem;
  animation: text-in 4s cubic-bezier(0.22, 0.15, 0.25, 1.43) 0s backwards;

}



.button {
  animation: flashing 2s ease-out;
  font-size: 1.4em;
  font-weight: bold;
  padding: 10px 30px 15px 30px;
  -moz-border-radius: 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  left: 45%;
  top: 60%;
  text-align: center;
  letter-spacing: 0.2em;
  width: 10%;
  height: 2.2em;
  position: absolute;
  color: rgb(126, 190, 190);
  text-decoration: none;
  transition: .4s;
  border: 2px solid rgb(126, 190, 190);
  border-radius: 4px;
}

.button:hover {
  background-color: rgb(126, 190, 190);
  border-color: rgb(126, 190, 190);
  color: #FFF;
}

.title {
  font-size: 180%;
  text-align: center;
  padding: 17%;
  letter-spacing: 0.9em;
  font-weight: 800;
  width: 100%;
  height: 45%;
  position: absolute;
  
}

@media screen and (max-width: 768px){

.title{
  font-size: 90%;
  padding: 27%;

}

.button{
  padding: 10px 90px 40px 20px;
} 
}
 
</style>
