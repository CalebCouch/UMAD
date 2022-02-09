<template>
  <div class="Register" id="Register">
    <div class="Register-Content">
      <div class="Register-Left" id="Register-Left">
        <p class="H1 B header" style="margin-top: 12.5%; margin-bottom: 2.5%;padding-top: 5%;">Apply</p>
        <!-- <p class="H6 L subtext" style="width: 80%;"></p> -->
        <div class="Form">
          <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="Form-Content">
            <div class="Form-Left">
              <p class="H6 M form-header">In Game Name</p>
              <b-form-input
                id="input-1"
                v-model="form.name"
                type="text"
                name="name"
                required
              ></b-form-input>
               <p class="H6 M form-header" style="width: 80%;">Describe your playstyle</p>
              <b-form-textarea
                id="textarea-5"
                v-model="form.playstyle"
                type="text"
                name="playstyle"
                required
              ></b-form-textarea>
              <p class="H6 M form-header" style="width: 80%;">Please Select The Team You Are Applying To</p>
              <select v-model="form.team" name="team" class="role">
                <option disabled value="">Please Select The Team You Are Applying To</option>
                <option>UMAD X</option>
                <option>UMAD Y</option>
                <option>UMAD Z</option>
                <option>Any team that will take me</option>
              </select>
              <b-button type="submit" class="Register-Button">Apply Now</b-button>
            </div>
            <div class="Form-Right">
              <p class="H6 M form-header">Best Times To Play (Expected to show up for at least one of these hours daily)</p>
              <b-form-textarea
                id="textarea-1"
                v-model="form.time"
                type="text"
                name="time"
                required
              ></b-form-textarea>

              <p class="H6 M form-header">Anoying Times To Play (We will only use these for hard to schedule scrims)</p>
              <b-form-textarea
                id="textarea-2"
                v-model="form.time2"
                type="text"
                name="time2"
                required
              ></b-form-textarea>

               <p class="H6 M form-header">Times Deffinently Unable to Play (We won't even ask if you can play durring these times)</p>
              <b-form-textarea
                id="textarea-3"
                v-model="form.time3"
                type="text"
                name="time3"
                required
              ></b-form-textarea>
              <p class="H6 M form-header" style="width: 80%;">Any other notes about times avalible</p>
              <b-form-textarea
                id="textarea-4"
                v-model="form.time4"
                type="text"
                name="time4"
                required
              ></b-form-textarea>
            </div>
          </b-form>
        </div>
        
      </div>
    </div>
  </div>
</template>

<script>
import emailjs from '@emailjs/browser';
export default {
  name: 'Register',
  data () {
    return {
      form: {
          name: '',
          time: '',
          time2: '',
          time3: '',
          time4: '',
          playstyle: '',
          team: '',
        },
        show: true
    }
  },
  methods: {
    onSubmit(e) {
      e.preventDefault()
      try {
        emailjs.sendForm('service_8qvkcdk', 'template_i93wfcv', e.target,
        'user_RvnnQps43K7mAMAI1SDN3', {
          name: this.name,
          time: this.time,
          time2: this.time2,
          time3: this.time3,
          time4: this.time4,
          playstyle: this.playstyle,
          team: this.team
        })
        alert('registration successful')
      } catch(error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.time = ''
      this.time2 = ''
      this.time3 = ''
      this.time4 = ''
      this.playstyle = ''
      this.team = ''

    },
    onReset(event) {
      event.preventDefault()
      // Reset our form values
     this.name = ''
      this.time = ''
      this.time2 = ''
      this.time3 = ''
      this.time4 = ''
      this.playstyle = ''
      this.team = ''
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .Register-Button {
    border: 0px;
    height: 5vh;
    border-radius: 100px;
    width: 100%;
    align-items: center;
    text-align: center;
    color: white;
    display: flex;
    margin-top: 5%;
    margin-bottom: 5%;
    background-color: #00B1FF;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    cursor: pointer;
  }

  .form-header {
    text-align: left;
    margin-top: 5% !important;
    margin-bottom: 2.5%!important;
  }

  .Register {
    width: 100vw;
    display: flex;
    margin-top: 5vw;
  }

  .Register-Content {
    width: 87.5vw;
    margin:auto;
    display: flex;
    flex-direction: row;
  }

  .Register-Left, Register-Right {
  }

  .Register-Right {
    width: 90vw;
  }

  .Register-Left {
    width: 100%;
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    box-shadow: 0 0 3vw 0.6vw lightgrey;
  }

  .Form {
    width: 70%;
    margin: auto;
    margin-top: 5%;
    margin-bottom: 10%;
  }
  .Form-Content {
    display: flex;
    flex-direction: row;
  }


  .Form-Right {
    margin-left: auto!important;

  }
  .Form-Left {
    margin-right: 10vw;

  }
  .role {
    display: block;
    width: 100%;
    height: calc(1.5em + 0.75rem + 2px);
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    border-radius: 0.25rem;
  }

</style>
