<template>
  <carousel :interval="8000" @defineInterval="handleIntervalChange" full>
    <carousel-indicators>
      <carousel-indicator :index="0" :class="{active: show[0]}" @changeSlide="handleChangeSlide"></carousel-indicator>
      <carousel-indicator :index="1" :class="{active: show[1]}" @changeSlide="handleChangeSlide"></carousel-indicator>
      <carousel-indicator :index="2" :class="{active: show[2]}" @changeSlide="handleChangeSlide"></carousel-indicator>
    </carousel-indicators>
    <carousel-inner>
      <carousel-item :class="{active: show[0]}" img :src="images.carousel2" mask="black-slight" alt="First slide">
      </carousel-item>
      <carousel-item :class="{active: show[1]}" img :src="images.carousel3" mask="black-slight" alt="Second slide">
      </carousel-item>
      <carousel-item :class="{active: show[2]}" img :src="images.carousel1" mask="black-slight" alt="Third slide">
      </carousel-item>
    </carousel-inner>
    <carousel-navigation @changeSlide="handleChangeSlide"></carousel-navigation>
  </carousel>
</template>

<script>
import {
  Carousel,
  CarouselIndicators,
  CarouselIndicator,
  CarouselInner,
  CarouselItem,
  CarouselNavigation,
  ViewWrapper,
  MdMask
} from "mdbvue";

import Carousel1 from "@/assets/img/carousel/carousel1.jpg"
import Carousel2 from "@/assets/img/carousel/carousel2.jpg"
import Carousel3 from "@/assets/img/carousel/carousel3.jpg"

export default {
  name: "CarouselPage",
  components: {
    Carousel,
    CarouselIndicators,
    CarouselIndicator,
    CarouselInner,
    CarouselItem,
    CarouselNavigation,
    ViewWrapper,
    MdMask
  },
  data() {
    return {
      page: 0,
      items: "",
      interval: 10000,
      show: {
        0: true,
        1: false,
        2: false,
        3: false,
        4: false,
        5: false,
        6: false,
        7: false,
        8: false,
        9: false
      },
      images: {
        carousel1: Carousel1,
        carousel2: Carousel2,
        carousel3: Carousel3,
      }
    };
  },
  methods: {
    slidePage(target) {
      if (target === "next") {
        if (this.page < this.items) {
          this.show[this.page] = false;
          this.page++;
          this.show[this.page] = true;
        } else {
          this.show[this.page] = false;
          this.page = 0;
          this.show[this.page] = true;
        }
      } else if (target === "prev") {
        if (this.page == 0) {
          this.show[this.page] = false;
          this.page = this.items;
          this.show[this.page] = true;
        } else {
          this.show[this.page] = false;
          this.page--;
          this.show[this.page] = true;
        }
      } else {
        this.show[this.page] = false;
        this.page = target;
        this.show[this.page] = true;
      }
    },
    autoSlide() {
      this.slide = setInterval(() => {
        this.slidePage("next");
      }, this.interval);
    },
    handleChangeSlide(showSlide) {
      this.slidePage(showSlide.slideIndex);
      clearInterval(this.slide);
      this.autoSlide();
    },
    handleIntervalChange(defineInterval) {
      this.interval = defineInterval.newInterval;
    }
  },
  mounted() {
    this.items = this.$el.querySelectorAll(".carousel-item").length - 1;
    this.autoSlide();
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.carousel {
  overflow: hidden;
}
.carousel,
.carousel-item,
.carousel-item.active {
  height: 100%;
}

.carousel-inner {
  position: relative;
  overflow: hidden;
}

.carousel-item {
  display: block !important;
  visibility: hidden;
  height: 0;
  opacity: 0;
  transition: transform 0ms ease-in-out, opacity 0.6s ease-in;
  transform: translate3d(0, 0, 0) !important;
}

.carousel-item.active {
  opacity: 1;
  left: auto;
  height: auto;
  visibility: visible;
  transform: translate3d(0, 0, 0) !important;
}
</style>
