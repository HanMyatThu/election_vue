

<template>
  <div>
    <gmap-map
      ref="gmap"
      :center="center"
      :zoom="8"
      style="width:100%;  height: 100vh;"
    >
      
      <gmap-marker
        :key="index"
        v-for="(m, index) in markers"
        :position="m.position"
        :clickable="true"
        :draggable="true"
        @click="toggleInfoWindow(m,index)">
      </gmap-marker>

      <gmap-info-window
        :options="infoOptions"
        :position="infoWindowPos"
        :opened="infoWinOpen"
        @closeclick="infoWinOpen=false"
      >
        <div v-html="infoContent"></div>
      </gmap-info-window>

    </gmap-map>
  </div>
</template>

<script>
  export default {
    name: "GoogleMap",
    data() {
      return {
        //a default center for the map
        center: {lat: 16.716564793705007, lng:95.77040086197871},
        map: null,
        infoContent: '',
        infoWindowPos: {
          lat: 0,
          lng: 0
        },
        infoWinOpen: false,
        currentMidx: null,
        //optional: offset infowindow so it visually sits nicely on top of our marker
        infoOptions: {
          pixelOffset: {
            width: 0,
            height: -35
          }
        },
        markers: [
          {
            name: "Bago",
            description: "Located in Bago Division",
            date_build: "",
            position: {lat: 17.33521, lng: 96.48135}
          },
          {
            name: "Mandalay",
            description: "Located in Mandalay Division",
            date_build: "",
            position: {lat: 21.97473, lng:  96.08359}
          },
          {
            name: "Maw La Myaing City",
            description: "Located in Mon State",
            date_build: "",
            position: {lat: 16.49051, lng:  97.62825}
          },
          {
            name: "Nay Pyi Taw City",
            description: "Captial City of Myanmar. Located in Mandalay Division",
            date_build: "",
            position: {lat: 19.745, lng: 96.12972}
          },
          {
            name: "Yangon City",
            description: "Located in Yangon Division",
            date_build: "",
            position: {lat: 16.80528, lng:  96.15611}
          },
          {
            name: "TaungGyi City",
            description: "Shan State",
            date_build: "",
            position: {lat: 20.78919, lng:  97.03776}
          },
          {
            name: "Pathein City",
            description: "Sagaing Division",
            date_build: "",
            position: {lat: 16.77919, lng:   94.73212}
          }, 
        ],
      };
    },
    
    methods: {
      toggleInfoWindow: function (marker, idx) {
        this.infoWindowPos = marker.position;
        this.infoContent = this.getInfoWindowContent(marker);
        

        //check if its the same marker that was selected if yes toggle
        if (this.currentMidx == idx) {
          this.infoWinOpen = !this.infoWinOpen;
        }
        //if different marker set infowindow to open and reset current marker index
        else {
          this.infoWinOpen = true;
          this.currentMidx = idx;
        }
      },

      getInfoWindowContent: function (marker) {
        return (`<div class="card">
  
      <div class="card-body">
        <div class="media">
          <div class="media-content">
            <p class="title is-4">${marker.name}</p>
          </div>
        </div>
        <div class="content">
          ${marker.description}
          <br>
          <time datetime="2016-1-1">${marker.date_build}</time>
        </div>
      </div>
    </div>`);
      },
    }
  };
</script>
