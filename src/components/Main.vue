<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'

export default {
  name: 'Main',
  components: {
    VueperSlides,
    VueperSlide 
  },
  data() {
    return {
      homeActive: true,
      aboutActive: false,
      projectsActive: false,
      front: 'Hi, my name is Michelle Giang and this is my story',
      slides: [
        {
          path: require('../assets/propic1.jpg'),
          description: '2016 - High School Graduation'
        },
        {
          path: require('../assets/DominicanRepublic2011.jpg'),
          description: '2011 - Vacation in Dominican Republican'
        },
        {
          path: require('../assets/Yellowstone20122.jpg'),
          description: '2012 - Vacation in Yellowstone Park'
        },
        {
          path: require('../assets/GrandTeton20123.jpg'),
          description: '2012 - Vacation in Grand Teton'
        },
        {
          path: require('../assets/ArchesNationalPark2012.jpg'),
          description: '2012 - Vacation in Arches National Park'
        },
        {
          path: require('../assets/Hawaii20134.jpg'),
          description: '2013 - Vacation in Hawaii'
        },
        {
          path: require('../assets/California2014.jpg'),
          description: '2014 - Vacation in California'
        },
        {
          path: require('../assets/propic3.jpg'),
          description: '2016 - Siebel Computer Science building at UIUC'
        },
        {
          path: require('../assets/Chicago20172.jpg'),
          description: '2017 - Trip to Chicago'
        },
        {
          path: require('../assets/propic.jpg'),
          description: '2017 - Study Abroad in POSTECH South Korea'
        },
        {
          path: require('../assets/Banff20172.jpg'),
          description: '2017 - Vacation in Banff Canada'
        },
        {
          path: require('../assets/AbbVie2018.jpg'),
          description: '2018 - Team won hackathon during internship at AbbVie'
        },
        {
          path: require('../assets/Greece2018.jpg'),
          description: '2018 - Vacation in Santorini Greece'
        },
        {
          path: require('../assets/Greece20182.jpg'),
          description: '2018 - Vacation in Kalambaka Greece'
        },
        {
          path: require('../assets/Target2019.jpg'),
          description: '2019 - Demo Day for internship at Target'
        }
      ]
    };
  },
  methods: {
    handleScroll() {
      var header = document.getElementById("headerContainer");
      var pic = document.getElementById("pic");
      if (document.body.scrollTop > 10 || document.documentElement.scrollTop > 10) {
        header.style.height = "8vh";
        header.style.fontSize = "3vh";
        pic.style.height = "8vh";
        pic.style.width = "4vw";
      } else {
        header.style.height = "10vh";
        header.style.fontSize = "4vh";
        pic.style.height = "10vh";
        pic.style.width = "5vw";
      }
      var main = document.getElementById("main");
      var about = document.getElementById("about");
      var projects = document.getElementById("projects");

      var mainOffset = main.offsetTop;
      var aboutOffset = about.offsetTop;
      var projectsOffset = projects.offsetTop;
      var pageOffset = window.pageYOffset;
      
      var padding = window.innerHeight*0.3;

      if (pageOffset >= (mainOffset-padding) && pageOffset < (aboutOffset-padding)) {
        this.homeActive = true;
        this.aboutActive = false;
        this.projectsActive = false;
      } else if (pageOffset >= (aboutOffset-padding) && pageOffset < (projectsOffset-padding)) {
        this.homeActive = false;
        this.aboutActive = true;
        this.projectsActive = false;
      } else {
        this.homeActive = false;
        this.aboutActive = false;
        this.projectsActive = true;
      } 
    },
    activeLink(link) {
      if (link === "main") {
        this.homeActive = true;
        this.aboutActive = false;
        this.projectsActive = false;
      } else if (link === "about") {
        this.homeActive = false;
        this.aboutActive = true;
        this.projectsActive = false;
      } else {
        this.homeActive = false;
        this.aboutActive = false;
        this.projectsActive = true;
      }
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
}
</script>

<template>
  <div class="home">
    <div class="headerContainer" id="headerContainer">
      <a class="propic" href="#">
        <img class="pic" src="../assets/propic.png" id="pic">
      </a>
      <a class="name" href="#"> Michelle Giang</a>
      <div class="pages">
        <a class="homeLink" v-bind:class="{active: homeActive}" href="#" v-on:click="activeLink('main')"> Home </a>
        <a class="aboutLink" v-bind:class="{active: aboutActive}" href="#about" v-on:click="activeLink('about')"> About </a>
        <a class="projectsLink" v-bind:class="{active: projectsActive}" href="#projects" v-on:click="activeLink('projects')"> Projects </a>
      </div>
    </div>
    <div class="mainContainer" id="main">
      <vueper-slides class="carousel" autoplay :bullets-outside="true" :touchable="false" :pauseOnHover="false" fixed-height="85vh" :fade="true">
        <vueper-slide v-for="(slide, idx) in slides" :key="idx" 
        :image="slide.path">
        <div slot="slideContent">
          <div class="transbox">
            <p class="title"> {{front}} </p>
            <p class="content"> {{slide.description}} </p>
          </div>
        </div>
        </vueper-slide>
      </vueper-slides>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.active {
  text-decoration: underline;
  color: #ebebeb;
}

.headerContainer {
  display: grid;
  grid-template-columns: 10% 40% 1fr;
  grid-template-areas: "left middle right";
  background: #aa1111;
  font-size: 4vh;
  color:  #c1c1c1;
  height: 10vh;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  position: fixed;
  top: 0px;
  width: 100%;
  z-index: 999;
}

.propic {
  grid-area: left;
  align-self: center;
  text-align: center;
}

.pic {
  margin-left: 2vw;
  width: 5vw;
  height: 10vh;
}

.name {
  text-decoration: none;
  align-self: center;
  color:  #c1c1c1;
  cursor: pointer;
}

.pages {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-areas: "linkHome linkAbout linkProj";
  color:  #c1c1c1;
  align-self: center;
  cursor: pointer;
}

.homeLink {
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
}

.aboutLink {
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
}

.projectsLink {
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
}

a {
  color:  #c1c1c1;
  text-decoration: none;
}

.homeLink:hover {
  color:#ebebeb
}

.aboutLink:hover {
  color:#ebebeb
}

.projectsLink:hover {
  color:#ebebeb
}

.mainContainer {
  background-color:#003A66;
  margin-top: 10vh;
}

.transbox {
  padding-left: 1vw;
  padding-right: 1vw;
  background-color: #ffffff;
  border: 1px solid black;
  opacity: 0.7;
}

.title {
  font-size: 3.5vw;
}

.content {
  font-size: 2vw; 
  color: #97640c;
}

.vueperslide {
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  color: #AA1111;
  font-style: bold;
}

</style>
