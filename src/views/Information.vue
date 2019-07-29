<template>
  <div>
    <div class="dark-section">
    <div class="container-fluid">
      <div class="row justify-content-center text-center" id="demos">
        <div class="col-lg-8">
        <h2>Preparing for voting</h2>
        <p class="lead">The rules are written by the Government. The 
    results are written by us.</p>
        </div>
      </div>
      <div class="row" style="margin-top: 30px;">
        <div class="col-md-4 col-lg-4 text-center pt-5">
            <div class="step_box"
            v-on:mouseover="mouseover('box')"
            v-on:mouseleave="mouseleave('box')" 
            v-bind:style= "shadow"
            >
            <div class="info">
              <h3>Step: 1</h3>
              <p>Things to know before entering the booth</p>
            </div>
            <div class="info_img">
              <img src="../assets/images/step1.svg" alt="step:1">
            </div>
            <hr>
            <div class="info_button">
              <button class="btn">Read More  <i class="fas fa-long-arrow-alt-right"></i> </button>
            </div>
          </div>  
        </div>
        <div class="col-md-4 col-lg-4 text-center pt-5 ">
          <div class="step_box"
            v-on:mouseover="mouseover('box1')"
            v-on:mouseleave="mouseleave('box1')" 
            v-bind:style= "shadow1"
            >
          <div class="info">
              <h3>Step: 1</h3>
              <p>Things to know before entering the booth</p>
          </div>
            <div class="info_img">
            <img src="../assets/images/step2.png" alt="step:1">
            </div>
          <hr>
          <div class="info_button">
            <button class="btn">Read More  <i class="fas fa-long-arrow-alt-right"></i> </button>
          </div>
          </div>  
        </div>  
        <div class="col-md-4 col-lg-4 text-center pt-5">
          <div class="step_box"
            v-on:mouseover="mouseover('box2')"
            v-on:mouseleave="mouseleave('box2')" 
            v-bind:style= "shadow2"
            >
            <div class="info">
            <h3>Step: 3</h3>
            <p>Explore the political party positions</p>
          </div>
          <div class="info_img">
            <img src="../assets/images/setp3.svg" alt="step:1">
          </div>
          <hr>
          <div class="info_button">
            <button class="btn">Read More  <i class="fas fa-long-arrow-alt-right"></i> </button>
          </div>
          </div>  
        </div>  
        <div class="col-md-4 col-lg-4 text-center pt-5">
          <div class="step_box"
            v-on:mouseover="mouseover('box3')"
            v-on:mouseleave="mouseleave('box3')" 
            v-bind:style= "shadow3"
            >
            <div class="info">
            <h3>Step: 4</h3>
            <p>After the election is not easy</p>
          </div>
          <div class="info_img">
            <img src="../assets/images/step4.png" alt="step:1">
          </div>
          <hr>
          <div class="info_button">
            <button class="btn">Read More  <i class="fas fa-long-arrow-alt-right"></i> </button>
          </div>
          </div>  
        </div>  
        <div class="col-md-4 col-lg-4 text-center pt-5 ">
          <div class="step_box"
            v-on:mouseover="mouseover('box4')"
            v-on:mouseleave="mouseleave('box4')" 
            v-bind:style= "shadow4"
            >
            <div class="info">
              <h3>Step: 5</h3>
              <p>In addition to entering the public booth</p>
            </div>
            <div class="info_img">
              <img src="../assets/images/step5.jpg" alt="step:1">
            </div>
            <hr>
            <div class="info_button">
              <button class="btn">Read More  <i class="fas fa-long-arrow-alt-right"></i> </button>
            </div>
          </div>  
        </div>
        <div class="col-md-4 col-lg-4 text-center pt-5">
          <div class="voting_image">
            <img src="../assets/images/voting.png" alt="voting">
          </div>
        </div>      
      </div>
      
    </div>    
    
  </div>
  <Items />
  <Footer />
  </div>
</template>

<script>
import Items from '../components/layout/Items'
import Footer from '../components/layout/Footer'

export default {
  components: {
    Items,
    Footer
  },
  data() {
    return {
      hover: false,
      shadow: "",
      shadow1: "",
      shadow2: "",
      shadow3: "",
      shadow4: "",
    }
  },
  methods: {
    mouseover: function(option){
      switch(option) {
        case "box":
          this.shadow =  "box-shadow: 5px 15px 25px grey;";
          break;
        case "box1":
          this.shadow1 =  "box-shadow: 5px 15px 25px grey;";
          break;
        case "box2":
          this.shadow2 =  "box-shadow: 5px 15px 25px grey;";
          break;
        case "box3":
          this.shadow3 =  "box-shadow: 5px 15px 25px grey;";
          break;
        case "box4":
          this.shadow4 =  "box-shadow: 5px 15px 25px grey;";
          break;
        default:
          break;
          
      }   

    },    
    mouseleave: function(option){
      switch(option) {
        case "box":
          this.shadow =  "box-shadow: none;";
          break;
        case "box1":
          this.shadow1 =  "box-shadow: none;";
          break;
        case "box2":
          this.shadow2 =  "box-shadow: none;";
          break;
        case "box3":
          this.shadow3 =  "box-shadow: none;";
          break;
        case "box4":
          this.shadow4 =  "box-shadow: none;";
          break;
        default:
          break;
          
      }   
    }
  }
}
</script>

