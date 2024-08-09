<template>
  <div id="app" class="app-background">
    <div class="q-pa-md">
      <div>
        <div>
          <DialogBoxRight
              message="jkdkkkkkkkkkkkkkkkkkkkkkkhdjsdadd ddasdkkkkkkkkkkkkk"
          />
       
        </div>

        <div style="margin-top: 20px;">
          <DialogBoxRightLeft 
             message="jkdkkkkkkkkkkkkkkkkkkkkkkhdjsdadd ddasdkkkkkkkkkkkkk"
          />
        </div>

        <div style="margin-top: 20px;">
            <dialogBoxAudio   :audioSrc="audioFile01"  :imageProfile="imageProfile"/>
          </div>
          <div style="margin-top: 20px;">
            <dialogBoxAudio   :audioSrc="audioFile02" :imageProfile="imageProfile"/>
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
import dialogBoxAudio from './components/dialogBoxAudio.vue';

export default {
  name: 'App',
  components: {
    MapComponent,
    DialogBoxRightLeft,
    DialogBoxRight,
    dialogBoxAudio
    
  },
  data() {
    return {
      audioFile01: require('@/assets/audio/benca.mp3'),
      audioFile02: require('@/assets/audio/audi01.mp3'),
      imageProfile: require('@/assets/image/perfilPersonagem02.jpeg')
    };
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
