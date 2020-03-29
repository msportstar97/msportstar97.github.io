<script>
export default {
  name: 'SelfBrand',
}
</script>

<template>
  <div class="selfBrand" id="selfBrand">
    <h3> Self Brand </h3>
    <h4> Self-Analysis </h4>
    <p> Looking at my strengths and weaknesses, 
      I realize that some of my strengths can also turn into weaknesses.
      I am someone who is very open. My main strength is being able to befriend many people I meet.
      I am sociable and can figure out ways to relate with others. I also have values I am loyal to, 
      though I respect other people's opinions. This can also be a weakness in a way as when I have to make
      decisions, I am not as open-minded. I am also very persistent, which could be a weakness especially as a CS major
      as I become too focused on a bug rather than moving on to other parts of a project and figuring out the bugs later. 
      Sometimes I become too focused on meeting deadlines as well and would work a 24/7 schedule even when I am stuck, when
      I should have taken a break and come up with ideas with a refreshed mind.
    </p>
    <img class="self" src="../assets/self.jpg">
    <h4> External-Analysis </h4>
    <p>
      I've asked a couple of my friends and family about their thoughts on my personality.
      The main strength that everyone mentions is that I am friendly to talk to. 
      I am able to build relationships with many different types of people. I like to forge personal
      connections with other people, making them feel comfortable. I also make the best of most situations.
      Other strengths my friends and family have mentioned is that I am confident in my skill. I won't say I am confident,
      but I do show it. I am also a dedicated and passionate person. I am a persistent person, especially when looking for
      solutions to issues. However, a main weakness that everyone mentions is that I am stubborn to a fault.
      At times, I am set on what I believe is right and could be very hard to convince to change opinions. 
      This often results in me not being open to compromise. Another weakness is that I am often overly careful.
      I end up stressing a lot about minute details even when it is not necessary. Another weakness is that I 
      am not good at time management. I get distracted easily at times. 
    </p>
    <img class="friend1" src="../assets/Friends1.jpg">
    <img class="friend2" src="../assets/Friends2.jpg">
    <h4> Congruence </h4>
    <p>
      Looking at my analysis versus my friends and family analyses, there are many similarities.
      I am not surprised by what other people have said about me as I am a pretty open book to read.
      There are a few things that I did not mention as my strength/weakness that my external sources did mention.
      Some of my friends and family have mentioned that I am a confident person. I don't believe that I am confident,
      often questioning many choices. However, I think people believe I am confident is because I sometimes internalize those questions
      rather than voicing my doubts. Even when I voice my doubts, I sound confident because they are doubts I firmly believe in.
      Everyone mentioned that I am stubborn, which I believe is true to a point the more I think about it. I believe 
      my stubbornness is due to my persistent and loyal nature. It could range from what brand to use 
      (i.e. Papa Johns, a cheaper option, or a local pizza store with better pizza taste) to professional choices 
      (i.e. a website should be designed with certain colors vs another option). As for loyalty, I am loyal to certain brands
      and would like to keep supporting them as they offer many benefits to loyal customers. In professional settings,
      the loyalty is towards the people who I believe have good ideas, and I would support them even if others disagree. 
      If I don't persist in what I believe is the best choice, then people would believe that I am not as confident in my own ideas,
      and my own opinions would not be considered. It does take awhile to convince me to change my mind, but that is because
      I would like confident alternatives that would actually work. People also mentioned that I often pay attention to little details,
      and that is true as I believe that every little detail should count, especially in coding projects as they could later come back
      as bugs which could make many other parts not work. I also think that my attention to little details is the main cause for why
      I do not have good time management skills. I have set deadlines, but I end up focusing on many of the little bugs rather than moving
      on to other parts and getting back to the bugs later, which ends up extending the timeline. After review of the analyses though,
      I do believe that I should learn to be more open to other options and let some things go for later times. 
    </p>
    <img class="postech" src="../assets/POSTECH.jpg">
    <img class="target" src="../assets/Target.jpg">
    <h4> Feature-Benefit </h4>
    <p> 
      I am a sociable person who is loyal to their values. I love communicating with other people and being able to find
      common ground with them. Even if we have nothing in common, I manage to find ways to befriend them. I may be stubborn 
      at times, but that is because I am loyal to things, whether it be brands or people. Being loyal can go far in terms of
      networking with other people or gaining benefits from companies. Overall, I am someone who can network with others and
      make the best of situations, and who will persist at looking other alternative solutions to issues.
    </p>
  </div>
</template>

<style scoped>
.selfBrand {
  margin-left: auto;
  margin-right: auto;
  padding-top: 8vh;
  padding-bottom: 5vh;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  font-size: 1.5vw;
  color: #d6a247;
  text-align: center;
  background-color:#1669a8;
}

p {
  margin-left: 10vw;
  margin-right: 10vw;
  font-size: 1.3vw;
}

img {
  margin: 5vw;
}

.self {
  transform: rotate(90deg);
  width: 20vw;
  height: 20vh;
}

.friend1 {
  width: 33vw;
  height: 38vh;
}

.friend2 {
  width: 33vw; 
  height: 35vh;
}

.postech {
  width: 30vw;
  height: 33vh;
}

.target {
  width: 30vw;
  height: 30vh;
}
</style>