<template>
  <div v-if="topic == 'athlets'">
    <img
      src="../assets/image/img-1-desktop.png"
      class="h-img-athlete hidden sm:hidden md:hidden lg:block xl:block 2xl:block 3xl:block"
      alt=""
    />
    <img
      src="../assets/image/img-athlets-tablet.png"
      class="h-img-athlete hidden sm:hidden md:block lg:hidden xl:hidden 2xl:hidden"
      alt=""
    />
  </div>

  <div v-else>
    <img
      src="../assets/image/img-basketball-desktop.png"
      class="h-img-players hidden sm:hidden md:hidden lg:block xl:block 2xl:block 3xl:block"
      alt=""
    />
    <img
      src="../assets/image/img-basketball-tablet.png"
      class="h-img-players hidden sm:hidden md:block lg:hidden xl:hidden 2xl:hidden"
      alt=""
    />
  </div>
</template>

<script>
export default {
  name: "ImageContent",
  props: {
    topic: { type: String, required: false },
  },
};
</script>

<style lang="css" scoped></style>
