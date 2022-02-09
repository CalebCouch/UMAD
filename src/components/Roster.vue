<template>
  <div class="Teams" id="Roster">
    <div class="Teams-Content">
      <div class="Teams-Header H1">
        Roster
      </div>
      <div class="Teams-Body">
        <table id="customers">
  <tr>
    <th>In game name</th>
    <th>Discord Tag</th>
    <th>Team</th>
    <th>Role</th>
    <th>Best Times</th>
    <th>Annoying Times</th>
    <th>Blackout Times</th>
  </tr>
  <tr>
    <td>QuantumTiger</td>
    <td>QuantumTiger#0407</td>
    <td>UMAD X</td>
    <td>Scheduler</td>
    <td>8:30-9:30PM EST Daily</td>
    <td>6:00-7:30PM EST Daily</td>
    <td>7:30-8:30PM EST Daily</td>
  </tr>

  
</table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Roster',
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

  #customers {
    font-family: Arial, Helvetica, sans-serif;
    border-collapse: collapse;
    width: 100%;
  }

  #customers td, #customers th {
    border: 1px solid #ddd;
    padding: 8px;
  }

  #customers tr:nth-child(even){background-color: #f2f2f2;}

  #customers tr:hover {background-color: #ddd;}

  #customers th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    background-color: #00B1FF;
    color: white;
  }
  


</style>
