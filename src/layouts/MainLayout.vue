<template>
  <div v-for="x in 6" :key="x" :class="'bubble bubble-' + x">
    
  </div>
  <div class="q-pa-md q-gutter-sm">
      <q-img
        src="src/assets/yoga-purple.png"
        spinner-color="white"
        style="height: 800px; max-width: 800px"
      />
    </div>
  <!-- <div class="line">asdasd</div>
    <div class="mouth">asdasd</div> -->
</template>

<script setup>
defineOptions({
  name: "MainLayout",
});
</script>
<style lang="scss">
body {
  background-image: linear-gradient(
    to bottom right,
    #91defe,
    #99c0f9,
    #bdb6ec,
    #d7b3e3,
    #efb3d5,
    #f9bccc
  );
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  overflow: hidden;
}
$bubbles_total: 6;

.bubble {
  height: 200px;
  width: 200px;
  border-radius: 50%;
  position: absolute;
  z-index: 1;
  background: radial-gradient(
    circle at 75% 30%,
    white 5px,
    aqua 8%,
    darkblue 60%,
    aqua 100%
  );
  @for $bubble from 1 through $bubbles_total {
    &-#{$bubble} {
      opacity: (random(60)) * 0.01;
      left: #{random(100)}vw;
      top: #{random(100)}vh;
    }
  }
  box-shadow: inset 0 0 20px #fff, inset 10px 0 46px #eaf5fc,
    inset 88px 0px 60px #c2d8fe, inset -20px -60px 100px #fde9ea,
    inset 0 50px 140px #fde9ea, 0 0 90px #fff;
}
// .bubble-2 {
//   height: 200px;
//   width: 200px;
//   border-radius: 50%;
//   position: relative;

//   background: radial-gradient(
//     circle at 75% 30%,
//     white 5px,
//     aqua 8%,
//     darkblue 60%,
//     aqua 100%
//   );
//   box-shadow: inset 0 0 20px #fff, inset 10px 0 46px #eaf5fc,
//     inset 88px 0px 60px #c2d8fe, inset -20px -60px 100px #fde9ea,
//     inset 0 50px 140px #fde9ea, 0 0 90px #fff;
// }

// .line {
//   height: 300px;
//   width: 100px;
//   background-color: red;
//   position: absolute;
//   top: 550px;
//   left: 150px;
//   border-bottom-left-radius: 40px;
//   border-bottom-right-radius: 40px;
// }

// .mouth {
//   height: 120px;
//   width: 200px;
//   position: absolute;
//   top: 850px;
//   left: 100px;
//   border-bottom-left-radius: 40px;
//   border-bottom-right-radius: 40px;
//   background-color: red;
//   position: absolute;
// }
</style>
