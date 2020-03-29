<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'

export default {
  name: 'About',
  components: {
    VueperSlides,
    VueperSlide 
  },
  data() {
    return {
      slides: [
        {
          path: require('../assets/home.jpg'),
        },
        {
          path: require('../assets/Bahamas2009.jpg'),
        },
        {
          path: require('../assets/HongKong2011.jpg'),
        },
        {
          path: require('../assets/Yellowstone2012.jpg'),
        },
        {
          path: require('../assets/GrandTeton20122.jpg'),
        },
        {
          path: require('../assets/Hawaii2013.jpg'),
        },
        {
          path: require('../assets/Hawaii20131.jpg'),
        },
        {
          path: require('../assets/Hawaii20132.jpg'),
        },
        {
          path: require('../assets/Hawaii20133.jpg'),
        },
        {
          path: require('../assets/California20141.jpg'),
        },
        {
          path: require('../assets/California20142.jpg'),
        },
        {
          path: require('../assets/Cali2014.jpg'),
        },
        {
          path: require('../assets/Cali20141.jpg'),
        },
        {
          path: require('../assets/UniversalStudios2015.jpg'),
        },
        {
          path: require('../assets/QuebecCity2016.jpg'),
        },
        {
          path: require('../assets/Disney2016.jpg'),
        },
        {
          path: require('../assets/Banff20171.jpg'),
        },
        {
          path: require('../assets/Banff20173.jpg'),
        },
        {
          path: require('../assets/Banff20174.jpg'),
        },
        {
          path: require('../assets/Chicago2017.jpg'),
        },
        {
          path: require('../assets/Chicago20173.jpg'),
        },
        {
          path: require('../assets/Greece20181.jpg'),
        },
        {
          path: require('../assets/Greece20183.jpg'),
        },
        {
          path: require('../assets/Greece20184.jpg'),
        },
        {
          path: require('../assets/StMartin20191.jpg')
        }
      ]
    }
  }
}
</script>

<template>
  <div class="about" id="about">
    <vueper-slides autoplay :bullets="false" :arrows="false" :touchable="false" 
    :pauseOnHover="false" fixed-height="95vh" :fade="true" :transitionSpeed="100" :speed="5000">
      <vueper-slide v-for="(slide, idx) in slides" :key="idx" 
      :image="slide.path" class="carousel">
        <div slot="slideContent">
          <div class="transbox">
            <h2 class="aboutTitle"> About </h2>
            <p class="aboutText"> I am a fun-loving woman looking for 
              a job opportunity in order to bring to life my programming skills in Java,
              JavaScript, HTML, SQL, and other languages to 
              program applications that could be shared with everyone.
              I am currently pursuing a bachelor's in computer science 
              with a minor in business. I am interested in the human-computer interaction
              field, putting to use my business knowledge in order to design and market web applications. 
            </p>
            <div class="moreAbout">
              <div class="hobbies">
                <h3> Hobbies </h3>
                <ul>
                  <li>Listen to EDM, i.e. Illenium, Said the Sky, Seven Lions</li>
                  <li>Watch crime shows, i.e. Criminal Minds, NCIS, and football</li>
                  <li>Photography (All the background pictures were taken from my vacations)</li>
                  <li>Watch animated and action movies</li>
                  <li>Going to beach and amusement parks</li>
                  <li>Spontaneous outings</li>
                  <li>Travelling</li>
                  <li>Skiing</li>
                </ul>
              </div>
              <div class="education">
                <h3> Education </h3>
                <h4>2016 - 2020</h4>
                <p>University of Illinois at Urbana-Champaign; Class of 2020
                  <br>
                  Bachelor of Science; Computer Science Major, Business Minor
                </p>
                <h4>2017</h4>
                <p>Pohang University of Science and Technology, Pohang, South Korea
                  <br>
                  Study Abroad Research in IOT
                </p>
              </div>
              <div class="experience">
                <h3> Experience </h3>
                <h4> June 2019 - Aug 2019</h4> 
                <p> Target, Software Engineer Intern</p>
                <h4> April 2018 - Present</h4> 
                <p> AbbVie, Rapid Application Developer Intern</p>
                <h4> June 2017 - July 2017</h4>
                <p> Pohang University of Science and Technology, Undergraduate Researcher</p>
                <h4> Feb 2016 - Aug 2016</h4>
                <p> Bloomberg, Software Engineer Intern</p>
              </div>
            </div>
          </div>
        </div>
      </vueper-slide>
    </vueper-slides>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.about {
  padding-top: 8vh;
}

.carousel {
  padding-top: 2vh;
}

.transbox {
  padding-left: 1vw;
  padding-right: 1vw;
  background-color: #ffffff;
  border: 1px solid black;
  opacity: 0.8;
}

.vueperslide {
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  font-size: 1.3vw;
  color: #0f5286;
  font-style: bold;
}

.aboutText {
  width: 75%;
  margin-left: auto;
  margin-right: auto;
}

.moreAbout {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas: "hobbies" "education" "experience";
  grid-column-gap: 5vw;
  width: 80vw;
  margin-left: auto;
  margin-right: auto;
  text-align: left;
}

li {
	list-style-position: outside;
}

h3 {
  margin-bottom: 1.5vh;
}

h4 {
  margin-bottom: 0;
  margin-top: 0;
}

p {
  margin-top: 1vh;
}
</style>