<template>
    <div @click="rotatingHam" :class="rotate">
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
    </div>
</template>


<script>
    import Vue from "vue";
    export default {
        name: "Burger",
        props: {
            rotate: String,
        },
        methods: {
           rotatingHam () {
                console.log("changed")
          }
        },
    }


</script>


<style scoped>
      /* .container {
  display: block;
  position: relative;
  top: -1050px;
  left: -320px;

  cursor: pointer;
  } */
  .world {
    text-align: center;
  }

.bar1, .bar2, .bar3 {
  width: 40px;
  border-radius: 20px;
  height: 5.5px;
  background-color: #2c3e50;
  margin: 6px 0;
  transition: 0.4s;
}

/* Rotate first bar */
.change .bar1 {
  -webkit-transform: rotate(-45deg) translate(-9px, 6px) ;
  transform: rotate(-45deg) translate(-8px, 6px) ;
}

/* Fade out the second bar */
.change .bar2 {
  opacity: 0;
}

/* Rotate last bar */
.change .bar3 {
  -webkit-transform: rotate(45deg) translate(-8px, -8px) ;
  transform: rotate(45deg) translate(-10px, -8px) ;
}

</style>
