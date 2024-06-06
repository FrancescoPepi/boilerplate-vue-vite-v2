<script>
import { store } from "../../data/store";

export default {
  data() {
    return {
      store,
      title: "Footer SubComponent",
      img: "/img/footer-ad-grid.png",
    };
  },

  // 	methods:{
  // 		myMethods(){
  // 			...
  // 		},
  // 	},

  // components: {
  //	MyComponent,
  // },

  // 	props:{
  // 		passaggioInfo: stringa,
  //  	 },
};
</script>

<template>
  <div class="bg">
    <div class="container py-5">
      <div class="row text-center">{{ title }}</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.bg {
  background-color: lightcoral;
  border: 2px dashed black;
  color: white;
}
</style>
