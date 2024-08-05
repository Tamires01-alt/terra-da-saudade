<template>
  <div id="app" class="app-background">
    <div class="q-pa-md">
      <div>
        <div>
          <DialogBoxRight/>
       
        </div>

        <div style="margin-top: 20px;">
          <DialogBoxRightLeft/>
        </div>
      </div>
      
       <div style="margin-left: 900px;;">
        <MapComponent/>
       </div>
       
    </div>
  </div>
</template>

<script>

import MapComponent from './components/map.vue';
import DialogBoxRight from './components/dialogBoxRight.vue';
import DialogBoxRightLeft from './components/dialogBoxLeft.vue';

export default {
  name: 'App',
  components: {
    MapComponent,
    DialogBoxRightLeft,
    DialogBoxRight
    
  }
};
</script>

<style scoped>
.app-background {
  background-image: url(assets/image/backgroundDark.jpeg);
  min-height: 100vh;
  margin: 0;
}
</style>
