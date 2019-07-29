<template id="countdown-template">
  <countdown :time="120 * 24 * 60 * 60 * 1000">
    <template slot-scope="props">
        <Slider />
        <div class="container">
          <div class="row main-feature">
            <div class="col-md-4">
              <div class="img-thumbnail">
                <img src="../assets/images/reliable.png" alt="Reliable">
              </div>
              <div class="caption">
                <h4>Secure & Reliable</h4>
                <p>All the data on the webiste is reliable blah blah blah blah.</p>
              </div>
            </div>
            <div class="col-md-4">
              <div class="img-thumbnail">
                <img src="../assets/images/realtime.png" alt="Real-time">
              </div>
              <div class="caption">
                <h4>Real Time Data</h4>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem officiis, autem dolores eum placeat veniam enim eaque tempore doloremque, cupiditate iste numquam at, suscipit temporibus. Maiores impedit fugiat quidem doloremque.</p>
              </div>
            </div>
            <div class="col-md-4">
              <div class="img-thumbnail">
                <img src="../assets/images/friendly.png" alt="User Friendly">
              </div>
              <div class="caption text-center">
                <h4>User Friendly</h4>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores omnis impedit temporibus est illum architecto nisi, placeat at, perferendis quibusdam exercitationem vel? Velit esse aspernatur iusto quo alias eveniet. Iusto?</p>
              </div>
            </div>    
          </div>
          <hr>
          <div class="row FeatLayout">
            <div class="col-md-5 Featimg"> <img src="../assets/images/myanmar.png" alt="feature" class="img-responsive center-block"></div>
            <div class="col-md-7">
                <h1>Electoral Parties and Places</h1>
                <p class="lead">Different parties and places blah blah</p>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt, a? Libero eveniet itaque eos, impedit numquam, error necessitatibus delectus maiores molestiae cumque placeat, enim facilis assumenda quas natus reprehenderit nostrum?</p>
                <ul class="ticklist">
                  <li><i class="far fa-check-circle"></i> Option 1</li>
                  <li><i class="far fa-check-circle"></i> Option 2</li>
                  <li><i class="far fa-check-circle"></i> Option 3</li>
                  <li><i class="far fa-check-circle"></i> Option 4</li>
                  <li><i class="far fa-check-circle"></i> Option 5</li>
                  <li><i class="far fa-check-circle"></i> Option 6</li>
                </ul>
                <div class="feat_actions text-center">
                  <router-link to="/election"
                  class="btn feature_btn_outline">
                    <span class="feat_btn_text">
                      Go to Election
                    </span>
                    <span class="feat_btn_text_icon">
                      <i class="far fa-hand-point-right"></i>
                    </span>
                  </router-link>
                </div>
            </div>
          </div>
          <hr>
          <div class="row FeatLayout" style="margin-top: 50px;">
            <div class="col-md-7">
                <h1>Election Information</h1>
                <p class="lead">To know more about Election</p>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores error sequi nisi, repellat mollitia at minus veritatis eum corporis? Vero esse nemo vel assumenda debitis cupiditate consectetur laboriosam minus in?</p>
                <ul class="ticklist" style="margin-bottom: 30px;">
                  <li><i class="far fa-check-circle"></i> Prepare</li>
                  <li><i class="far fa-check-circle"></i> Option2</li>
                  <li><i class="far fa-check-circle"></i> Option 3</li>
                  <li><i class="far fa-check-circle"></i> Option 4</li>
                  <li><i class="far fa-check-circle"></i> Option 5</li>
                  <li><i class="far fa-check-circle"></i> Option 6</li>
                </ul>
                <div class="feat_actions text-center">
                  <router-link to="/information"
                  class="btn feature_btn_outline">
                    <span class="feat_btn_text">
                      Go to Information
                    </span>
                    <span class="feat_btn_text_icon">
                      <i class="far fa-hand-point-right"></i>
                    </span>
                  </router-link>
                </div>
            </div>
            <div class="col-md-5 Featimg">
               <img src="../assets/images/election.png" alt="feature" class="img-responsive center-block"></div>
            
          </div>
        </div> 
        <div id="dont-miss-it" style="margin-top : 50px;">
          <div class="image-divider auto-height" data-stellar-background-ratio="0.3">
            <div class="container" style="background: #00000099; min-height: 420px;">                 	 
              <div class="row">
                <div class="col-md-8 offset-md-2 text-center">                   	
                  <h2 id="dont-miss-it-title" class="text-center animation pt-2 fadeInUp">Don't Miss It!</h2>                                                    
                      <div class="text-center animation fadeInUp">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ultrices malesuada ante quis pharetra. Nullam non bibendum dolor. Ut vel turpis accumsan, efficitur dolor fermentum, tincidunt metus. Etiam ut ultrices nibh.  Etiam aliquam mauris non hendrerit faucibus. Proin pulvinar congue  ex, vitae commodo. Phasellus condimentum, mi ut sodales gravida.</p>
                      </div>  
                                
                  </div>
              </div>
                        
              <div class="row">     				
                <div class="col-xs-2 offset-xs-2 col-md-2 offset-md-2">
                  <div class="countdown-col-wrapper text-center">
                    <h1>{{ props.days }}  Days</h1>
                  </div>
                </div>
                <div class="col-xs-2 col-md-2">
                  <div class="countdown-col-wrapper text-center">
                    <h1>{{ props.hours }}  Hours</h1>
                  </div>
                </div>
                <div class="col-xs-2 col-md-2">
                  <div class="countdown-col-wrapper text-center">
                    <h1>{{ props.minutes }}  Minutes</h1>
                  </div>
                </div>
                <div class="col-xs-2 col-md-2">
                  <div class="countdown-col-wrapper text-center">
                    <h1>{{ props.seconds }}  Seconds</h1>
                  </div>
                </div>
                    
              </div>
                        
            </div>
                
          </div>
        </div>
      <MoveTop />
      <Footer />
    </template>
  </countdown>
</template>

<script>
import MoveTop from '../components/layout/MoveTop'
import Footer from '../components/layout/Footer'
import Slider from '../components/layout/Slider'

export default {
  components: {
    MoveTop,
    Footer,
    Slider
  },
  methods: {
    transform(props) {
      Object.entries(props).forEach(([key, value]) => {
        // Adds leading zero
        const digits = value < 10 ? `0${value}` : value;

        // uses singular form when the value is less than 2
        const word = value < 2 ? key.replace(/s$/, '') : key;

        props[key] = `${digits} ${word}`;
      });

      return props;
    },
  },
};

</script>
