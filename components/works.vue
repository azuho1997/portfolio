<template>
  <div class="boder">
    <div class="title">
      Works
      <font-awesome-icon icon="laptop" />
    </div>
      <div class="letter">
        <div class="git"> 
          This site
          <a class="link" href="https://github.com/ohuzak-1997/portfolio">
              <span class="fas fa-heart fa-2x" style="color: rgb(45, 119, 119)">
                <font-awesome-icon :icon="['fab','github']" />
              </span>
          </a>
      </div>
      <div class="photo">
      <img src="~/assets/2020-05-13.png" width="400px" height="220px">
      <img src="~/assets/2020-05-15.png" width="400px" height="220px">
      </div>
    </div>
  </div>
</template>

<style scoped>
.boder {
  border: solid 6px aliceblue;
  color:#FFF;
  margin-top: 2%;
  padding: 1% 1% 10% 4%; 
  height: 55vh;
}
.title {
  font-size: 180%;
  border-bottom: solid 6px aliceblue;
  padding-left: 8%;
  /* margin-bottom: 4%; */
  padding-bottom: 2%;
}

img{
  border: rgb(214, 183, 207) solid 4px;
}

/* a{
 display: inline-block;
} */

.git{
  text-align: center;
  margin-bottom: 2%;
}
.photo{
  text-align: center;
}

</style>
