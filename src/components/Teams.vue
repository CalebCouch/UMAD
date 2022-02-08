<template>
  <div class="Teams" id="Teams">
    <div class="Teams-Content">
      <div class="Teams-Header H1">
        Current UMAD Clan Teams
      </div>
      <div class="Teams-Body">
        <div class="Team">
          <p class="H3">UMAD X</p>
          <p class="H4">Practice time: 8:30-9:30 PM EST Daily</p>
          <p class="H4">Captian: SoupLaddler</p>
          <img class="Rimage" src="../assets/logo.png">
          <div class="Register H4">Apply</div>
        </div>
        <div class="Team">
          <p class="H3">UMAD Y</p>
          <p class="H4">Practice time: 8:00-9:00 PM EST Daily</p>
          <p class="H4">Captian: Ghost Maker</p>
          <img class="Rimage" src="../assets/logo.png">
          <div class="Register H4">Apply</div>
        </div>
        <div class="Team">
          <p class="H3">UMAD Z</p>
          <p class="H4">Practice time: 7:30-8:30 PM EST Daily</p>
          <p class="H4">Captian: Cerberus</p>
          <img class="Rimage" src="../assets/logo.png">
          <div class="Register H4">Apply</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Teams',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .Floating-Image {
    top: 120%;
    left: 60%;
    position: absolute;
  }

  .Teams {
    width: 100vw;
    display: flex;
    margin-top: 5vw;
  }
  .Teams-Content {
    width: 87.5vw;
    margin:auto;
    box-shadow: 0 0 3vw 0.6vw lightgrey;
  }
  .Teams-Header {
    width: 100%;
    heigth: 5%;
    margin: auto;
    padding-top: 5%;
    margin-top: 5%;
    margin-bottom: 5%;
    display: flex;
    text-align: center;
    flex-direction: column;
  }
  .Teams-Body {
    width: 85%;
    heigth: 100%;
    margin: auto;
    margin-top: 5%;
    padding-bottom: 10%;
    display: flex;
    text-align: center;
    flex-direction: row;
  }

  .Team {
    box-shadow: 0 0 3vw 0.6vw lightgrey;
    margin-left: 2.5%;
    margin-right: 2.5%;
    padding-top: 2.5%;
    height: 50vh;
  }

  .Register{
    height: 5vh;
    margin: auto!important;
    margin-top: 10%!important;
    border-radius: 100px;
    width: 80%;
    text-align: center;
    color: white;
    display: flex;
    background-color: #00B1FF;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    cursor: pointer; 
  }

  .Rimage {
    width: 75%;
  }
  


</style>
