<template>
    <div id="app">
        <div class="container">
          <Header>

          </Header>
          <swiper
            :modules="modules"
            :slides-per-view="1"
            :space-between="50"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
            navigation
            :pagination="{clickable: true}"

          >
            <swiper-slide>
              <div class="testslider">dddd</div>
            </swiper-slide>
            <swiper-slide>
              <div class="testslider">dsdad</div>
            </swiper-slide>
            <swiper-slide>
              <div class="testslider">dsadsa</div>
            </swiper-slide>

            
          </swiper>
        </div>
    </div>
</template>

<script>
import Header from './components/Header.vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Pagination, Scrollbar, A11y } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';

export default {
  name: 'App',
  components: {
    Header,
    Swiper,
    SwiperSlide,
  },
  setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Navigation, Pagination, Scrollbar, A11y],
      };
    },
}
</script>

<style>
body{
  background-color: #1C1C1E;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container{
  width: 86%;
  margin: 0 auto;
}
.testslider{
  width: 100%;
  height: 800px;
  background-color: blue;
}
</style>
