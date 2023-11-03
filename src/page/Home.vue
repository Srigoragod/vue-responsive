<template>
  <div class="">
    <ContentCard
      class="hidden sm:hidden md:block xl:block 2xl:block"
      v-for="(item, index) in items"
      :key="index"
      :title="item.topic"
      :items="item.contents"
    />

    <MobileSlider
      class="show-mobile hidden sm:block md:hidden xl:hidden 2xl:hidden"
      v-for="(item, index) in items"
      :key="index"
      :title="item.topic"
      :items="item.contents"
    ></MobileSlider>
  </div>
</template>

<script>
import ContentCard from "../components/ContentCard.vue";
import MobileSlider from "../components/MobileSlider.vue";
export default {
  name: "Home",
  components: {
    ContentCard,
    MobileSlider,
  },
  data() {
    return {
      items: [
        {
          topic: "athlets",
          contents: [
            {
              number: "01",
              title: "Connection",
              content:
                "Connect with coaches directly, you can ping coaches to view profile.",
            },
            {
              number: "02",
              title: "Collaboration",
              content:
                "Work with other student athletes to increase visibility. When you share and like other players videos, it will increase your visibility as a player. This is the team work aspect of Surface 1.",
            },
            {
              number: "03",
              title: "Growth",
              content:
                "Resources and tools for you to get better as a student Athelte. Access to training classes, tutor sessions, etc",
            },
          ],
        },
        {
          topic: "players",
          contents: [
            {
              number: "01",
              title: "Connection",
              content:
                "Connect with talented athlete directly, you can watch their skills through video showreels directly from Surface 1.",
            },
            {
              number: "02",
              title: "Collaboration",
              content:
                "Work with recruiter to increase your chances of finding talented athlete.",
            },
            {
              number: "03",
              title: "Growth",
              content: "Save your time, recruit proper athlets for your team.",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="css">
@media screen and (min-width: 1920px) {
  .show-mobile {
    display: none;
  }
}
@media screen and (min-width: 768px) and (max-width: 1919px) {
  .show-mobile {
    display: none;
  }
}
@media screen and (min-width: 320px) and (max-width: 767px) {
  .show-mobile {
    display: block;
  }
}
</style>
