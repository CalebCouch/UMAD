<template>
  <div class="FAQ" id="FAQ">
    <div class="FAQ-Content">
      <div class="FAQ-Body">
        <div class="FAQ-Header">
          <p class="H1 B">FAQ</p>
          <p class="H4">Since our curriculum is designed to teach kids typing, math, VIM, terminal, Javascript, HTML, and CSS, your kids will need to have already learned reading, addition and subtraction.</p>
        </div>
        <div class="accordion" role="tablist">
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-1 class="FAQ-Small-Header">
              <p class="H35 B">What are the kids going to be learning?</p>
              <img id="plus1" class="FAQ-image" src="../assets/plus.png">
              <img id="minus1" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-1" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">Each student will learn every skill that is imperative to programming.</p>
                <div class="FAQ-Nav-Button" v-on:click="scrollTo('Curriculum')">See the curriculum</div>
                 <div class="FAQ-Nav-Button2" style="display: none;" v-on:click="scrollTo('Curriculum')"><div class="H5 M" style="margin: auto!important;">Curriculum</div></div>
              </b-card-body>
            </b-collapse>
          </b-card>
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-2 class="FAQ-Small-Header">
              <p class="H35 B">Where is it located?</p>
              <img id="plus2" class="FAQ-image" src="../assets/plus.png">
              <img id="minus2" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-2" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">The program will be held in the Orlando, FL area. A location will be provided if you are accepted into the program</p>
              </b-card-body>
            </b-collapse>
          </b-card>
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-3 class="FAQ-Small-Header">
              <p class="H35 B">What time is it going to take place?</p>
              <img id="plus3" class="FAQ-image" src="../assets/plus.png">
              <img id="minus3" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-3" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">The program will be held weekly 1:00pm to 3:00pm on Tuesday</p>
              </b-card-body>
            </b-collapse>
          </b-card>
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-4 class="FAQ-Small-Header">
              <p class="H35 B">What do I need to bring?</p>
              <img id="plus4" class="FAQ-image" src="../assets/plus.png">
              <img id="minus4" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-4" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">You will need to bring a functioning laptop in order to participate in the program</p>
              </b-card-body>
            </b-collapse>
          </b-card>
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-5 class="FAQ-Small-Header">
              <p class="H35 B">How much will it cost?</p>
              <img id="plus5" class="FAQ-image" src="../assets/plus.png">
              <img id="minus5" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-5" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">The price is 195$ per month, However partial and full Shcolarships are available.</p>
              </b-card-body>
            </b-collapse>
          </b-card>
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-6 class="FAQ-Small-Header">
              <p class="H35 B">What’s the program’s schedule?</p>
              <img id="plus6" class="FAQ-image" src="../assets/plus.png">
              <img id="minus6" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-6" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">Each schedule will be different for each student. A schedule for your child will be provided on location.</p>
              </b-card-body>
            </b-collapse>
          </b-card>
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-7 class="FAQ-Small-Header">
              <p class="H35 B">Who’s going to be teaching?</p>
              <img id="plus7" class="FAQ-image" src="../assets/plus.png">
              <img id="minus7" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-7" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">Software developers Caleb and Jack Couch</p>
              </b-card-body>
            </b-collapse>
          </b-card>
          <b-card no-body class="mb-1 FAQ-Card">
            <div v-b-toggle.accordion-8 class="FAQ-Small-Header">
              <p class="H35 B">What’s the age range of the students?</p>
              <img id="plus8" class="FAQ-image" src="../assets/plus.png">
              <img id="minus8" class="FAQ-image" style="display: none;" src="../assets/minus.png">
            </div>
            <b-collapse class="acord" id="accordion-8" accordion="my-accordion" role="tabpanel">
              <b-card-body style="padding-left: 0!important;">
                <p class="H5 M">All of the students are required to be between the ages of eight to eighteen</p>
              </b-card-body>
            </b-collapse>
          </b-card>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FAQ',
  data () {
    return {
      toggles: [true, false]
    }
  },
  mounted () {
    const toggle = () => {
      const acords = Array.from(document.getElementsByClassName("FAQ-Small-Header"))
      for (var i = 0; i < acords.length; i++) {
        if (acords[i].getAttribute('aria-expanded') == 'true') {
          document.getElementById("plus"+(i+1)).style.display = 'none'
          document.getElementById("minus"+(i+1)).style.display = 'block'
        } else {
          document.getElementById("minus"+(i+1)).style.display = 'none'
          document.getElementById("plus"+(i+1)).style.display = 'block'
        }
      }
      setTimeout(() => {toggle()}, 10)
    }
    toggle()
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

  @media only screen and (max-width: 651px) {
    .FAQ-Content {
      box-shadow: 0 -1.2vw 0 0 #D8D8D8!important;
    }
    .FAQ-Card {
      z-index: 0!important;
    }
    .FAQ-image {
      margin-top: auto!important;
      margin-left: auto!important;
      margin-bottom: auto!important;
      height: 7vw!important;
    }
    .FAQ-Nav-Button {
      display: none!important;
    }
    .FAQ-Nav-Button2 {
      display: flex!important;
    }
  }
  
  .FAQ-Nav-Button {
    height: 5vh;
    border-radius: 100px;
    width: 50%;
    text-align: center;
    color: white;
    display: flex;
    margin-top: 5%;
    background-color: #00B1FF;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    cursor: pointer;
  }
  .FAQ-Nav-Button2 {
    height: 5vh;
    border-radius: 100px;
    width: 100%;
    text-align: center;
    color: white;
    display: flex;
    margin-top: 5%;
    background-color: #00B1FF;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    cursor: pointer;
  }

  .FAQ-Card {
    box-shadow: 0 0.4vw 0 0 #D8D8D8;
    text-align: left;
    border: 0!important;
    border-radius: 0px;
  }
  
  .FAQ-Small-Header {
    padding-top: 1vw;
    padding-bottom: 1vw;
    display:flex;
    flex-direction: row;
  }

  .FAQ-image {
    margin-left: auto;
    height: 100%;
  }

  .FAQ {
    width: 100vw;
    display: flex;
    margin-top: 5vw;
    margin-bottom: 5vw;
  }
  .FAQ-Content {
    width: 87.5vw;
    margin:auto;
    padding-bottom: 5vw;
    box-shadow: 0 0 3vw 0.6vw lightgrey;
  }
  .FAQ-Header {
    width: 100%;
    heigth: 5%;
    margin: auto;
    margin-top: 5%;
    margin-bottom: 5%;
    display: flex;
    text-align: center;
    flex-direction: column;
  }
  .FAQ-Body {
    width: 77.5%;
    heigth: 100%;
    margin: auto;
    margin-top: 5%;
    display: flex;
    text-align: center;
    flex-direction: column;
  }

</style>
