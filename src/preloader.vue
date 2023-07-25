<template>
  <div class="pre-loader" v-bind:style="{'background-color' : bgColor}"> 
    <slot>
      <div class="loader">
        <spinner class="icon"/>
        <p class="preloader_text" v-bind:style="{color : textColor}"> Loading.... </p>
      </div> 
    </slot> 
  </div>
</template> 

<script>
import spinner  from "./spinner.vue"

export default {
  data: () => {
    return {}
  },
  props: {
    bgColor : {
      type : [String],
      default : "white"
    },
    textColor : {
      type : [String],
      default : "black"
    },
  },
  methods: {},
  components : {
    spinner
  },
  mounted: () => {},
}
</script>
 
<style>
 
 .pre-loader {
    --padding : 5vh 10vw ;

    padding: var(--padding);
    position: fixed;
    top: 0;
    bottom: 0;
    left : 0;
    right : 0;
    display: flex;
    flex-direction: row;
    justify-content: center;
    height: 100vh;
    z-index: 100;
 }

 .icon {
    margin: 0vh 2vw;        
 }

 .loader {
    padding: 45vh;
    display: flex;
    flex-direction: row;
 }

 .preloader_text {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; /** check */
    margin: auto;
 }

 /**
  * check
  */
/*
 @media screen and (min-width: 400px) {
    .loader {
        padding :  0px;
    }
 }*/
 
</style>