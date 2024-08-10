<template>
  <div style="display: flex">
    <div class="boxStyleComponent7">
      <div id="map"></div>
    </div>
    <div class="ponteiroUser"></div>
  </div>
</template>

<script>
import L from "leaflet";
import "leaflet/dist/leaflet.css";
import "leaflet-routing-machine";
import "leaflet-routing-machine/dist/leaflet-routing-machine.css";

export default {
  name: "MapComponent",
  mounted() {
    const map = L.map("map").setView([51.505, -0.09], 13);

    L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
      attribution:
        '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
    }).addTo(map);

    L.Routing.control({
      waypoints: [L.latLng(-23.551, -46.633), L.latLng(-10.751, -39.208)],
      createMarker: function (i, waypoint) {
        var marker = L.marker(waypoint.latLng).bindPopup(
          i === 0 ? "Departure Point" : "Destination Point"
        );
        return marker;
      },
    }).addTo(map);
  },
};
</script>

<style>
#map {
  max-width: 470px;
  height: 200px;
  border-radius: 20px 20px 20px 20px;
}

.boxStyleComponent7 {
  width: 550px;
  min-height: 56px;
  padding: 30px 15px;
  border-radius: 20px 0px 20px 20px;
  background-color: #d9fdd3;
  text-align: center;
  color: #111b21;
}

@media only screen and (max-width: 600px) {
  .boxStyleComponent7 {
    width: 380px;
    min-height: 56px;
    padding: 30px 15px;
    border-radius: 20px 0px 20px 20px;
    background-color: #d9fdd3;
    text-align: center;
    color: #111b21;
  }
}

.ponteiroUser {
  background-color: #d9fdd3;
  border-radius: 0px 0px 400px 0px;
  width: 12px;
  height: 14px;
}
</style>
