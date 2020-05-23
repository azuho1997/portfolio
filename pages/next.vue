<template>
  <div>
    <div class="all">
      <Snowf
        :amount="50"
        :size="5"
        :speed="1.5"
        :wind="0"
        :opacity="0.8"
        :swing="1"
        :image="null"
        :zIndex="null"
        :resize="true"
        color="#fff"
      />
      <header>
        <p class="header">PORTFOLIO</p>
        <a class="menuButton" id="menuButton" @click="menu">
          <div></div>
          <div></div>
          <div></div>
        </a>
      </header>
      <div class="buttons">
        <nav>
          <div class="button">
            <div class="buttonName" @click="buttonTop">TOP</div>
            <toggle-button
              color="rgb(126, 190, 190)"
              @change="buttonTop"
              :value="topFlg"
              :sync="true"
              height="40"
              width="84"
            ></toggle-button>
          </div>
          <br />
          <div class="button">
            <div class="buttonName" @click="buttonAbout">ABOUT</div>
            <toggle-button
              color="rgb(126, 190, 190)"
              @change="buttonAbout"
              :value="aboutFlg"
              :sync="true"
              height="40"
              width="84"
            ></toggle-button>
          </div>
          <br />
          <div class="button">
            <div class="buttonName" @click="buttonWorks">WORKS</div>
            <toggle-button
              color="rgb(126, 190, 190)"
              @change="buttonWorks"
              :value="worksFlg"
              :sync="true"
              height="40"
              width="84"
            ></toggle-button>
          </div>
          <br />
          <div class="button">
            <div class="buttonName" @click="buttonSkills">SKILLS</div>
            <toggle-button
              color="rgb(126, 190, 190)"
              @change="buttonSkills"
              :value="skillsFlg"
              :sync="true"
              height="40"
              width="84"
            ></toggle-button>
          </div>
          <br />
          <div class="button">
            <div class="buttonName" @click="buttonPosts">POSTS</div>
            <toggle-button
              color="rgb(126, 190, 190)"
              @change="buttonPosts"
              :value="postsFlg"
              :sync="true"
              height="40"
              width="84"
            ></toggle-button>
          </div>
        </nav>
        <div class="detail">
          <transition name="fade">
            <top v-if="topFlg"></top>
            <about v-if="aboutFlg"></about>
            <works v-if="worksFlg"></works>
            <skills v-if="skillsFlg"></skills>
            <posts v-if="postsFlg"></posts>
          </transition>
        </div>
      </div>
      <footer>
        <a class="link" href="https://github.com/azuho1997/portfolio">
          <span class="fas fa-heart fa-4x" style="color: rgb(45, 119, 119)">
            <font-awesome-icon :icon="['fab','github']" />
          </span>
        </a>
        PORTFOLIO
      </footer>
    </div>
  </div>
</template>

<script>
import top from "~/components/top.vue";
import about from "~/components/about.vue";
import works from "~/components/works.vue";
import skills from "~/components/skills.vue";
import posts from "~/components/posts.vue";
import Snowf from "vue-snowf";

export default {
  components: {
    top,
    about,
    works,
    skills,
    posts,
    Snowf
  },
  data: function() {
    return {
      topFlg: true,
      aboutFlg: false,
      worksFlg: false,
      skillsFlg: false,
      postsFlg: false
    };
  },
  methods: {
    buttonTop: function() {
      this.topFlg = !this.topFlg;
      this.aboutFlg = false;
      this.worksFlg = false;
      this.skillsFlg = false;
      this.postsFlg = false;
    },
    buttonAbout: function() {
      this.topFlg = false;
      this.aboutFlg = !this.aboutFlg;
      this.worksFlg = false;
      this.skillsFlg = false;
      this.postsFlg = false;
    },
    buttonWorks: function() {
      this.topFlg = false;
      this.aboutFlg = false;
      this.worksFlg = !this.worksFlg;
      this.skillsFlg = false;
      this.postsFlg = false;
    },
    buttonSkills: function() {
      this.topFlg = false;
      this.aboutFlg = false;
      this.worksFlg = false;
      this.skillsFlg = !this.skillsFlg;
      this.postsFlg = false;
    },
    buttonPosts: function() {
      this.topFlg = false;
      this.aboutFlg = false;
      this.worksFlg = false;
      this.skillsFlg = false;
      this.postsFlg = !this.postsFlg;
    },
    menu: function(){
      
    }
  },
  transition: "test"
};
</script>



<style scoped>
.all {
  height: 100vh;
}

header {
  text-align: center;
  padding: 3%;
  background-size: cover;
  transition: opacity 0.24s ease-in;
  opacity: 0.5;
  color: rgb(208, 212, 216);
  font-size: 350%;
  font-weight: 1000;
  letter-spacing: 0.4em;
  -webkit-text-stroke: 3px rgb(45, 119, 119);
}

.menuButton {
  opacity: 0;
  /* display: block; */
  height: 60px;
  width: 60px;
  background: rgb(126, 190, 190);
  position: fixed;
  top: 0;
  right: 0;
}

.buttons {
  height: 75vh;
  display: flex;
  transition: opacity 0.24s ease-in;
}
.buttonName {
  transition: opacity 0.24s ease-in;
}
.buttonName:hover {
  opacity: 0.5;
}

nav {
  height: 75vh;
  width: 15%;
  border-right: solid 6px rgb(243, 245, 247);
  color: rgb(72, 76, 80);
  background: rgb(221, 218, 218);
  padding-top: 5%;
  font-size: 150%;
  font-weight: 700;
  letter-spacing: 0.2em;
  border-radius: 40px 40px 40px 40px;
}

.button {
  margin-inline-end: 55%;
  text-align: center;
}

.detail {
  height: 80vh;
  background-color: rgb(126, 190, 190);
  height: 75vh;
  width: 90%;
  padding: 3% 10% 10% 10%;
  font-size: 200%;
  border-radius: 40px 40px 40px 40px;
}

footer {
  border-top: solid 6px rgb(249, 251, 252);
  height: 8%;
  font-size: 100%;
  font-weight: 800;
  text-align: right;
  padding: 1%;
  color: rgb(31, 45, 46);
  background-size: cover;
  opacity: 0.5;
}

.detailsentence {
  color: rgb(72, 76, 80);
}

.fade-enter {
  opacity: 0;
}
.fade-enter-active {
  transition: opacity 500ms;
}
.fade-enter-to {
  opacity: 1;
}

font-awesome-icon {
  border-radius: 50%;
  transition: all 0.6s ease 0s;
}
font-awesome-icon:hover {
  cursor: pointer;
  transform: scale(1.1, 1.1);
}

@media screen and (max-width: 768px) {
  header {
    font-size: 180%;
  }

  nav {
    width: 0;
    opacity: 0;
  }
  .detail {
    margin-top: 20px;
    width: 100%;
  }

.menuButton {
  opacity: 1;
}
.menuButton div {
  height: 3px;
  width: 40px;
  background: #ffffff;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%); /*アニメーションは変更前のclassに付ける*/
  transition: 0.3s; /*3秒かけて変化する*/
}

.menuButton div:nth-of-type(1) {
  transform: translate(-50%, -15px);
}

.menuButton div:nth-of-type(3) {
  transform: translate(-50%, 12px);
}
}
</style>


