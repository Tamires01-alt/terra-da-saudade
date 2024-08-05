<template>
  <div>
    <GMapMap
      :center="center"
      :zoom="10"
      style="width: 100%; height: 500px"
    >
      <GMapMarker
        v-for="(marker, index) in markers"
        :key="index"
        :position="marker.position"
      />
      <GMapPolyline
        :path="routePath"
        :options="polylineOptions"
      />
    </GMapMap>
    
  </div>

</template>

<script>
import { GMapMap, GMapMarker, GMapPolyline } from '@fawmi/vue-google-maps';

export default {
  name: 'GoogleMaps',
  components: {
    GMapMap,
    GMapMarker,
    GMapPolyline,
  },
  data() {
    return {
      center: { lat: 37.7749, lng: -122.4194 }, // Default center (San Francisco)
      markers: [
        { position: { lat: 37.7749, lng: -122.4194 } }, // Starting point
        { position: { lat: 34.0522, lng: -118.2437 } }, // Destination
      ],
      routePath: [
        { lat: 37.7749, lng: -122.4194 }, // Starting point
        { lat: 34.0522, lng: -118.2437 }, // Destination
      ],
      polylineOptions: {
        strokeColor: '#FF0000',
        strokeOpacity: 1.0,
        strokeWeight: 2,
      },
    };
  },
};
</script>

<style scoped>
.boxStyleComponent{
    width: 50%;
    height: 256px;
    padding: 30px 15px;
    border-radius: 20px 0px 20px 20px ;
    background-color: #d9fdd3;
    text-align: center;
    color: #111b21;
}

.ponteiroUser{
    background-color: #d9fdd3;
    border-radius: 0px 0px 400px 0px ;
    width: 12px;
    height: 14px;
}
</style>
