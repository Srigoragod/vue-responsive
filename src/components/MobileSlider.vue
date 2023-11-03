<template>
  <div :class="title">
    <div class="header-title-h1 text-uppercase">
      {{ title }}
    </div>
    <ImageContent :topic="title" />
    <Splide :options="splideOptions">
      <SplideSlide v-for="(item, index) in items" :key="index">
        <div class="container-sub-title flex item-center">
          <div class="group-number">
            <div class="text-number">{{ item.number }}</div>
            <div class="number-underline"></div>
          </div>
          <div>
            <h3 class="title-h3 text-uppercase">{{ item.title }}</h3>
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
<style lang="css" scoped>
.container-sub-title {
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
.header-title-h1 {
  color: #e7e7e7;
  font-size: 3.125rem;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
</style>
