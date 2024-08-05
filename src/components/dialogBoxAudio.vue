<template>
    <div style="display: flex;">
        <div class="boxStyleComponent">
          <div style="display: flex;">
            <img :src="backgroundImage"   style="width: 60px; height: 60px; cursor: pointer;" >
           
              <q-slider v-model="standard" :min="6" :max="50" style="margin-top:14px;"/>
          
            
          </div>
        </div>
        <div class="ponteiroUser"></div>

        
    </div>
</template>
<script>
import backgroundImage from '@/assets/icon/play_arrow.svg';
import { ref } from 'vue'
export default {
  
 props: {
 },
 mounted() {
    
 },
  data() {
    return {
      standard: ref(28),
      backgroundImage
    };
  },
  methods: {
  }
}

</script>
<style>
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