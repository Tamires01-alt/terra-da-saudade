<template>
  <div style="display: flex"  class="positionBox">
    
    <div id="boxStyleComponentLeft3">
      <div>
        <img class="imageContent" :src="this.imageContent" />
      </div>
    </div>
    <div class="ponteiroUser"></div>
  </div>
</template>
<script>
export default {
  props: {
    imageContent: {
      type: String,
      required: true,
    },
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
<style>
#boxStyleComponentLeft3 {
  width: 550px;
  min-height: 56px;
  padding: 30px 15px;
  font-size: 18px;
  border-radius: 20px 0px 20px 20px;
  background-color: #d9fdd3;
  text-align: center;
  color: #111b21;
}

@media only screen and (max-width: 600px) {
  #boxStyleComponentLeft3{
    width: 380px;
    min-height: 56px;
    padding: 30px 15px;
    font-size: 18px;
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


.imageContent {
  max-width: 352px;
  max-height: 244px;
}

.positionBox {
   padding: 0px 0px 0px 190px ;
}

@media only screen and (max-width: 600px) {
  .positionBox {
    padding: 0px 0px 0px 0px;
  }
}
</style>