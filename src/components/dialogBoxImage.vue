<template>
    <div style="display: flex;">
        <div class="pointerUserLeft"></div>
        <div id="boxStyleComponentLeft3">
            <div>
                <img class="imageContent" :src="this.imageContent"/>
            </div>
        </div>
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
    return {
    };
  },
  methods: {
   
  },
};
</script>
<style>
#boxStyleComponentLeft3{
    width: 550px;
    min-height: 56px;
    padding: 30px 15px;
    border-radius: 0px 20px 20px 20px ;
    background-color: #f4f4f4;
    text-align: center;
    color: #0b141a;
}

.pointerUserLeft{
    background-color: #f4f4f4;
    border-radius: 0px 0px 0px 400px ;
    width: 12px;
    height: 14px;
}

.imageContent{
    width: 252px;
    height: 204px; 
}
</style>