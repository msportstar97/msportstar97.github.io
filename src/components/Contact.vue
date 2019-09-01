<script>
export default {
  name: 'Contact',
  props: {
    
  }
}
</script>

<template>
  <div class="contact">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="contactInfo">
      <div class="icons">
        <a href=https://www.facebook.com/michi.giang target="_blank">
          <i class="fa fa-facebook-square fb"></i></a>
        <a href=https://www.linkedin.com/in/michelle-giang target="_blank">
          <i class="fa fa-linkedin-square linkedin"></i></a>
        <a href=https://github.com/msportstar97 target="_blank">
          <i class="fa fa-github-square git"></i></a>
        <a href=https://www.youtube.com/channel/UCP3CMhrXNRrpxH2wr5loGFw/videos target="_blank">
          <i class="fa fa-youtube-square yt"></i></a>
      </div>
      <div class="resume">
        <a href="https://github.com/msportstar97/msportstar97.github.io/blob/sourceCode/src/assets/MichelleGiangResume.pdf" target="_blank" class="cv">
          <button class="btn">
              <i class="fa fa-download"></i> 
              Download Resume
          </button>
        </a>
      </div>
      <div class="details">
        <p class="info"> 
          michi.giang@gmail.com
        </p>
      </div>
    </div>
    <div class="footer">
      <i class="fa fa-copyright"><span class="copyright"> 2019 By Michelle Giang </span></i>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.contact {
  margin-left: auto;
  margin-right: auto;
  padding-top: 3vh;
  background-color: #7bbaeb;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  font-size: 2vw;
  color: black;
}

.contactInfo {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas: "icons resume details";
}

.icons {
  justify-self: center;
  align-self: center;
}

.fb {
  color:#3B5998;
  margin-right: 1vw;
}

.linkedin {
  color: #4875B4;
  margin-right: 1vw;
}

.git {
  margin-right: 1vw;
}

.yt {
  color: #FF3333;
  margin-right: 1vw;
}

.resume {
  justify-self: center;
  align-self: center;
}

.btn {
  color: #ecf8ff;
  background: #b4842f;
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  border: none;
  font-size: 1vw;
  cursor: pointer;
  padding: 2vh;
  border-radius: 1vh;
}

.btn:hover {
  color:  #f5f5a6;
}

.cv {
  text-decoration: none;
  color: #ebebeb;
}

.info {
  font-size: 1vw;
  color: black;
}

.footer {
  background: #AA1111;
  color: #ebebeb;
  padding: 3vh;
  font-size: 1vw;
  width: 100%;
  margin-top: 3vh;
}

.copyright {
  font-family: 'Proxima Nova Soft', 'Helvetica Neue', sans-serif;
  color: #ebebeb;
}
</style>