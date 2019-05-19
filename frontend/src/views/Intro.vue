<template>
  <section class="header">
    <video autoplay loop class="video-background" muted plays-inline>
      <source src="./../assets/videos/coffee.mp4" type="video/mp4">
    </video>

    <img class="logo" src="./../assets/images/socam-logo.png">
    <div class="welcome-msg">
      <h1>HELLO, SOCAM.</h1>
      <router-link to="/home" class="btn btn-connect">Connect</router-link>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  // name: "home"
  // components: {
  //   HelloWorld
  // }
};
</script>

<style scoped>
.header {
  height: 100vh;
}

.video-background {
  position: absolute;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: -1;
}

/*  
aspect-ratio, min-aspect-ratio, max-aspect-ratio (화면 비율)
: width/height 비율에 대응한다. 즉, width를 height로 나눈 값.

aspect-ratio:1
화면 비율이 1:1 인 경우에 대응하며 예를 들면 320*320, 640*640 등이 대응

aspect-ratio:16/9
계산식으로 사용하였으며 HDTV에 일반적인 화면 비율인 16:9 인 경우에 대응 (예: 1920*1080)
*/
@media (max-aspect-ratio: 16/9) {
  .video-background {
    width: auto;
    height: 100%;
  }
}

.logo {
  margin: -40px 0px 0px 10px;
  width: 250px;
  /* height: 40px; */
}

.welcome-msg {
  position: relative;
  text-align: center;
  color: #fff;
  top: 150px;
}

.welcome-msg h1 {
  font-size: 80px;
  font-weight: 200;
  letter-spacing: 5px;
  margin-bottom: 30px;
}

.btn {
  font-size: 25px;
  color: #fff;
  margin: 10px;
  padding: 10px 22px;
  text-decoration: none;
  border: 3px solid;
  border-radius: 25px;
}

.btn-subscribe:hover {
  background-color: #eb9940;
  transition: 0.5s;
}

.btn-connect:hover {
  background: #eb9940;
  transition: 0.5s;
}
</style>

