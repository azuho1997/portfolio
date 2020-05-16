<template>
  <div>
    <div class="boder">
        <span class="title">
            <div>Welcome</div>
            <br>
            <div>to my</div> 
            <br>  
            <div>portforio</div>
        </span>
    </div>
  </div>
</template>

<script>
  import { VueTyper } from 'vue-typer';


  export default {
    components: {
      VueTyper
    }
  }

</script>
<style scoped>
.boder {
  border: solid 6px aliceblue;
  color: rgb(72, 76, 80);  
  margin-top: 2%;
  padding: 10% 1% 10% 4%;
  height: 55vh;
}


.title {
  font-size: 180%;
  z-index: 1;
  color: #fff;
  line-height: 2rem; 
  letter-spacing: 0.15em;
  animation: text-fade 2s infinite linear; 
  line-height: 2rem;
  margin-top: 10%;
}

@keyframes text-fade {
  0% {
    opacity: 1;
  }
  25% {
    opacity: 0.8;
  }
  50% {
    opacity: 0.9;
  }
  75% {
    opacity: 0.6;
  }
}

</style>