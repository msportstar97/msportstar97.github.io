<script>
export default {
  name: 'Projects',
  data() {
    return {
      bobaShow: 'none',
      yimmyShow: 'none',
      toyShow: 'none'
    }
  },
  methods: {
    bobaOpen() {
      this.bobaShow = 'block';
      document.documentElement.style.overflow = "hidden";
    },
    bobaClose() {
      this.bobaShow = 'none';
      document.documentElement.style.overflow = "scroll";
    },
    yimmyOpen() {
      this.yimmyShow = 'block';
      document.documentElement.style.overflow = "hidden";
    },
    yimmyClose() {
      this.yimmyShow = 'none';
      document.documentElement.style.overflow = "scroll";
    },
    toyOpen() {
      this.toyShow = 'block';
      document.documentElement.style.overflow = "hidden";
    },
    toyClose() {
      this.toyShow = 'none';
      document.documentElement.style.overflow = "scroll";
    }
  }
}
</script>

<template>
  <div class="projects" id="projects">
    <h3> Projects </h3>
    <h4> BobaBuddy </h4>
    <p> Never had boba before? Need help deciding which boba to get?
      BobaBuddy is the app to help you find the right boba... and you can leave reviews!
    </p>
    <div class="modalButton">
      <button class="buttonModal" v-on:click="bobaOpen"> 
      Learn More </button></div>
    <div class="modalOverlay" v-bind:style="{ display: bobaShow }" v-on:click="bobaClose"></div>
    <div class="modal" v-bind:style="{ display: bobaShow }">
      <div class="modalContent">
        <button class="close" v-on:click="bobaClose"> Exit </button>
        <p> When people walk into a boba place, 
          they are often afraid of trying a new flavor/topping 
          in fear of the taste not suiting them.
          BobaBuddy is the place for people to search a boba store, 
          either manually or according to their location. 
          They could look at the menu and choose a boba to see the reviews for.
          The reviews includes ratings for specific preferences, 
          so people would know what kinds of preferences would be best.
          People can also login to the site and leave a review.
          All the user and boba place data are stored in a Firebase database.
          <br>
          Website: <a href="https://msportstar97.github.io/BobaBuddy" target="_blank">
          https://msportstar97.github.io/BobaBuddy </a>
          <br>
          Source Code: <a href="https://github.com/msportstar97/BobaBuddy" target="_blank">
          https://github.com/msportstar97/BobaBuddy </a>
        </p>
      </div>
    </div>
    <iframe width="50%" height="500vh" controls
    src="https://www.youtube.com/embed/seUSZPkMS3M">
    </iframe>
    <h4> Yimmy </h4>
    <p> Have a hard time choosing where to eat? Tired of eating the same stuff every day? Then Yimmy is the app for you.</p>
    <div class="modalButton">
      <button class="buttonModal" v-on:click="yimmyOpen"> 
      Learn More </button></div>
    <div class="modalOverlay" v-bind:style="{ display: yimmyShow }" v-on:click="yimmyClose"></div>
    <div class="modal" v-bind:style="{ display: yimmyShow }">
      <div class="modalContent">
        <button class="close" v-on:click="yimmyClose"> Exit </button>
        <p> As college students, 
          we are often faced with the complication of finding a place
          to eat while staying healthy. That's where Yimmy comes along. 
          Using Google API and Nutritionix API, 
          Yimmy will suggest meal options at local restaurants that 
          are filtered by location, cuisine type, caloric needs, and price range. 
          It will also generate a meal plan for the entire week according to your needs, 
          all of which is stored in our database. 
          You will also get a nutritional chart showcasing proteins, carbs, and fats assuming
          you eat at the suggested restaurants with the suggested meals in the meal plan.
          <br>
          Website: <a href="https://yimmplayground.web.illinois.edu/" target="_blank">
          https://yimmplayground.web.illinois.edu/ </a>
          <br>
          Source Code: <a href="https://github.com/msportstar97/Yimmy" target="_blank">
          https://github.com/msportstar97/Yimmy </a>
        </p>
      </div>
    </div>
    <iframe width="50%" height="500vh" controls
    src="https://www.youtube.com/embed/CyLQEV_6V8I">
    </iframe>
    <h4> ToySorty </h4>
    <p> A fun VR game for all ages. 
      Play different levels of taking apart toys
      and sorting them with powerups while avoiding bombs.</p>
    <div class="modalButton">
      <button class="buttonModal" v-on:click="toyOpen"> 
      Learn More </button></div>
    <div class="modalOverlay" v-bind:style="{display: toyShow}" v-on:click="toyClose"></div>
    <div class="modal" v-bind:style="{display: toyShow}">
      <div class="modalContent">
        <button class="close" v-on:click="toyClose"> Exit </button>
        <p> A VR sorting game with toy figures modeled after Big Hero 6's microbots. 
          A group of 5 teamed up to create this fun
          interactive game for not just kids, but also adults.
          This game puts the players in a toy room setting, 
          decorated with many toy figures with a nice back window view of mountains.
          There are a total of 4 different levels, 
          each with one little extra piece of the toy figure 
          they need to take apart. Each part of the toys will have 
          different ways to take them apart 
          (i.e. swinging the toy around to take off the head). 
          There are also power-ups (i.e. increase time) 
          that players could grab to help them beat a level. 
          Tutorials with videos are provided to assist players.
          <br>
          Source Code: <a href="https://github.com/msportstar97/ToySorty" target="_blank">
          https://github.com/msportstar97/ToySorty </a>
        </p>
      </div>
    </div>
    <iframe width="50%" height="500vh" controls
    src="https://www.youtube.com/embed/_ZzXodB8WVo">
    </iframe>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.projects {
  margin-left: auto;
  margin-right: auto;
  padding: 3vh;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  font-size: 1.5vw;
  color: #b4842f;
  text-align: center;
}

.modalButton {
  padding: 3vh;
}

.buttonModal {
  color: #ecf8ff;
  background: #b4842f;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  font-size: 1.5vw;
  border: none;
  border-radius: 1vh;
  padding: 1vw;
  width: 10vw;
}

.buttonModal:hover {
  color: #f5f5a6;
}

.modalOverlay {
  background: rgba(0, 0, 0, 0.2);
  position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
  z-index: 1;
}

.modal {
  background: #ecf8ff;
  max-height: calc(100% - 100px);
  position: fixed;
    top: 50%;
    left: 50%;
    right: auto;
    bottom: auto;
  transform: translate(-50%, -50%);
  z-index: 1;
  border-radius: 5vh;
}

.modalContent {
  color: #21213a;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  font-size: 1.5vw;
  margin-right: auto;
  margin-left: auto;
  padding: 5vh;
}

.close {
  color: #ecf8ff;
  background: #b4842f;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  font-size: 1.5vw;
  border: none;
  border-radius: 1vh;
  padding: 1vw;
  width: 5vw;
}

.close:hover {
  color: #f5f5a6;
}
</style>