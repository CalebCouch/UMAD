<template>
  <div class="BOX-ONE">
    <div class="small" style="display: none;">This website is not supported for this screen size please view on a larger device, We are working to fix this.</div>
    <div class="Header">
      <p class="logo-one H1">UMAD CLAN</p>
      <div class="nav-buttons">
        <div class="nav-button H5"v-on:click="scrollTo('Teams')">The Teams</div>
        <div class="nav-button H5" v-on:click="scrollTo('Roster')" >Roster</div>
        <div class="Register-button H5" v-on:click="scrollTo('Register-Left')">Apply</div>
      </div>
    </div>
    <div class="Content">
      <div class="Content-One">
        <video id="video1"
    muted="muted">
            <source src="../assets/UMADCLAN_Ninja_Intro.mp4" poster="../assets/UMADNINJA.jpg">
        </video>
      </div>
      
    </div>
    <div class="MC">
      <Teams></Teams>
      <Register></Register>
      <Roster></Roster>
      <div class="white-space"></div>
    </div>
  </div>
</template>

<script>
import Teams from './Teams'
import Register from './Register'
import Roster from './Roster'

export default {
  name: 'Main',
  components: {
    Teams,
    Register,
    Roster
  },
  data () {
    return {
    }
  },
  mounted () {
    var video = document.getElementById('video1')
    setTimeout(()=>{video.play()},1000)
    var FinishVideo = () => {
      console.log(video.networkState)
      if (video.currentTime >= 4.627744) {
        video.pause()
        return
      }
      setTimeout(() => {FinishVideo()}, 100)
    }
    FinishVideo()
  },
  methods: {
    scrollTo: (id) => {
      var target = document.getElementById(id)
      var scrollContainer = target;
      do { //find scroll container
          scrollContainer = scrollContainer.parentNode;
          if (!scrollContainer) return;
          scrollContainer.scrollTop += 1;
      } while (scrollContainer.scrollTop == 0);
      
      var targetY = 0
      if (window.screen.width < 651) {
        targetY+= -((window.screen.height / 100) * 10);
      }
      
      do { //find the top of target relatively to the container
          if (target == scrollContainer) break;
          targetY += target.offsetTop;
      } while (target = target.offsetParent);
      
      scroll = function(c, a, b, i) {
          i++; if (i > 30) return;
          c.scrollTop = a + (b - a) / 30 * i;
          setTimeout(function(){ scroll(c, a, b, i); }, 20);
      }
      // start scrolling
      scroll(scrollContainer, scrollContainer.scrollTop, targetY, 0);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#video1 {
  width: 100vw;
}
@media only screen and (max-width: 1007px) {
  .Header, .Content, .MC {
    display: none!important;
  }
  .small {
    display: block!important;
  }
}

@media only screen and (max-width: 651px) {
}

.white-space {
  width: 100%;
  height: 5vw;
}

.BOX-ONE {
  width:100vw;
  height:100vh;
}

.Content {
  display: flex;
  flex-direction: row;
}

.Content-One {
  width: 100%;
}

.Content-One-Nav-Button {
  position: absolute;
  bottom: 20vh;
  left: 5vw;
  height: 5vh;
  border-radius: 100px;
  width: 50%;
  text-align: center;
  color: white;
  display: flex;
  margin-top: 5%!important;
  background-color: #00B1FF;
  justify-content: center;
  align-content: center;
  flex-direction: column;
  cursor: pointer;
}

.Header {
  height: 10vh;
  width: 100%;
  background-color: black;
  display:flex;
}

.logo-one {
  height: 60%;
  margin-left: 5%!important;
  margin-top: auto!important;
  margin-bottom: auto!important;
  align-self: center;
  color: rgb(230, 60, 40);
  align-text: center;
}

.nav-buttons {
  font-size: 1.4vw;
  height: 100%;
  margin-left: auto!important;
  display: flex;
  padding-left: 5%;
  width: 35%;
}

.nav-button {
  align-self: center;
  margin-right: 10%!important;
  text-align: center;
  color: #FFFFFF;
  cursor: pointer;
}

.Register-button {
  align-self: center;
  width: 9vw;
  text-align: center;
  cursor: pointer;
  background-color: white;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-content: center;
  flex-direction: column;
  font-size: 1.2vw;
  height: 40%;
}

</style>
