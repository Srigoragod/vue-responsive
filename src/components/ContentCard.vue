<template>
  <div :id="title" class="">
    <ImageContent :topic="title" />
    <TopTitle :title="title" />
    <ContentItem
      :items="items"
      :isRight="title != 'athlets' ? true : false"
    ></ContentItem>
  </div>
</template>

<script>
import TopTitle from "./TopTitle.vue";
import ImageContent from "./ImageContent.vue";
import ContentItem from "./ContentItem.vue";
export default {
  name: "AthleteList",
  components: {
    TopTitle,
    ImageContent,
    ContentItem,
  },
  props: {
    title: String,
    items: Array,
  },
};
</script>
