<template id="countdown-template">
  <!-- need to fix this later -->
  <countdown :time="120 * 24 * 60 * 60 * 1000">
    <template slot-scope="props">
        <div id="dont-miss-it">
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
    </template>
  </countdown>
</template>

<script>

export default {
  name: "Countdown",
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
