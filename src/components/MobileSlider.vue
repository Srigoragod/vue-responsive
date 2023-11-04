<template>
  <div :class="title">
    <div class="header-title-h1-xs uppercase">
      {{ title }}
    </div>
    <img
      v-if="title == 'athlets'"
      src="../assets/image/img-athlets-mobile.png"
      class="h-img-athlete-xs"
      alt=""
    />
    <img
      v-else
      src="../assets/image/img-basketball-mobile.png"
      class="h-img-players-xs"
      alt=""
    />
    <Splide :options="splideOptions">
      <SplideSlide v-for="(item, index) in items" :key="index">
        <div class="container-sub-title-xs flex item-center">
          <div class="group-number">
            <div class="text-number">{{ item.number }}</div>
            <div class="number-underline"></div>
          </div>
          <div>
            <h3 class="title-h3 uppercase">{{ item.title }}</h3>
          </div>
        </div>
        <div class="text-content">
          {{ item.content }}
        </div>
      </SplideSlide>
    </Splide>
  </div>
</template>

<script>
import ImageContent from "./ImageContent.vue";
import ContentItem from "./ContentItem.vue";
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";

export default {
  components: {
    Splide,
    SplideSlide,
    ImageContent,
    ContentItem,
  },
  props: {
    title: { type: String, required: false },
    items: { type: Array, required: false },
  },
  data() {
    return {
      slides: [
        {
          title: "Slide 1",
          description: "Description for Slide 1",
          image: "slide1.jpg",
        },
        {
          title: "Slide 2",
          description: "Description for Slide 2",
          image: "slide2.jpg",
        },
        // Add more slides as needed
      ],
      splideOptions: {
        type: "carousel",
        perPage: 1,
        arrows: false,
        pagination: true,
      },
    };
  },
};
</script>

<style lang="css">
.container-sub-title-xs {
  padding-top: 1.063rem;
}
.splide__slide {
  background: #f5f4f9;
  padding: 4.5rem 1rem 4.313rem 1rem;
}
.splide__pagination__page {
  background: #d8d8d8;
  width: 0.625rem;
  height: 0.625rem;
  opacity: unset;
}
.splide__pagination {
  padding-bottom: 1.875rem;
}
.splide__pagination li {
  margin-right: 0.313rem;
}
.splide__pagination__page.is-active {
  background: #5c3caf;
  transform: unset;
  z-index: 1;
}
</style>
<style lang="css" scoped>
.header-title-h1-xs {
  color: #e7e7e7;
  font-size: 50px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.h-img-athlete-xs {
  max-height: 59.375rem;
  max-width: 42.375rem;
  position: relative;
  margin: 0 auto -5rem auto;
  z-index: 1;
}

.h-img-players-xs {
  position: relative;
  margin-bottom: -3.25rem;
  margin-top: 23px;
  margin-left: 0.5rem;
  z-index: 1;
}
</style>
