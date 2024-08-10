<template>
  <div id="app" class="app-background">
    <div class="q-pa-md">
      <div>
        <div class="alignItems">
          <DialogBoxRight
            message="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque eu bibendum elit. Sed pretium cursus facilisis. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed blandit at diam eu vestibulum. Quisque lorem metus, finibus eu massa vel, fringilla varius metus. Donec at finibus tellus. Aenean vitae viverra odio. Fusce nisl felis, viverra eget placerat at, venenatis sed purus. Sed eleifend maximus ipsum at placerat. Aenean lobortis viverra posuere. Pellentesque in efficitur nisl. Maecenas blandit nunc eget erat ornare, nec tincidunt arcu commodo. Mauris blandit id dolor et sodales. Sed tincidunt at lorem ut rhoncus."
          />

          <DialogBoxRightLeft
            message="jkdkkkkkkkkkkkkkkkkkkkkkkhdjsdadd ddasdkkkkkkkkkkkkk"
          />

          <dialogBoxAudio
            :audioSrc="audioFile01"
            :imageProfile="imageProfile"
          />
          <dialogBoxImage :imageContent="imageContent" />

          <MapComponent/>
        </div>
      </div>


     
       
      
    </div>
  </div>
</template>

<script>
 import MapComponent from './components/map.vue';
import DialogBoxRight from "./components/dialogBoxRight.vue";
import DialogBoxRightLeft from "./components/dialogBoxLeft.vue";
import dialogBoxAudio from "./components/dialogBoxAudio.vue";
import dialogBoxImage from "./components/dialogBoxImage.vue";

export default {
  name: "App",
  components: {
     MapComponent,
    DialogBoxRightLeft,
    DialogBoxRight,
    dialogBoxAudio,
    dialogBoxImage,
  },
  data() {
    return {
      audioFile01: require("@/assets/audio/benca.mp3"),
      audioFile02: require("@/assets/audio/audi01.mp3"),
      imageProfile: require("@/assets/image/perfilPersonagem02.jpeg"),
      imageContent: require("@/assets/image/perfilPersonagem02.jpeg"),
    };
  },
};
</script>

<style scoped>
.app-background {
  background-image: url("assets/image/backgroundDark.jpeg");
  min-height: 1050px;
}

.alignItems{
  display: flex;
  align-items: center;
  flex-direction: column;
  gap:20px;
}
</style>
