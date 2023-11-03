<template>
  <div v-if="topic == 'athlets'">
    <img
      src="../assets/image/img-athlets-desktop.png"
      class="custom-height-img-athlete hidden sm:hidden md:hidden xl:block 2xl:block"
      alt=""
    />
    <img
      src="../assets/image/img-athlets-tablet.png"
      class="custom-height-img-athlete hidden sm:hidden md:block xl:hidden 2xl:hidden"
      alt=""
    />

    <img
      src="../assets/image/img-athlets-mobile.png"
      class="custom-height-img-athlete show-mobile hidden sm:block md:hidden xl:hidden 2xl:hidden"
      alt=""
    />
  </div>

  <div v-else>
    <img
      src="../assets/image/img-basketball-desktop.png"
      class="custom-height-img-basketball hidden sm:hidden md:hidden xl:block 2xl:block"
      alt=""
    />
    <img
      src="../assets/image/img-basketball-tablet.png"
      class="custom-height-img-basketball hidden sm:hidden md:block xl:hidden 2xl:hidden"
      alt=""
    />
    <img
      src="../assets/image/img-basketball-mobile.png"
      class="custom-height-img-basketball show-mobile hidden sm:block md:hidden xl:hidden 2xl:hidden"
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

<style lang="css" scoped>
@media screen and (min-width: 1920px) {
  .custom-height-img-athlete {
    max-height: 59.375rem;
    max-width: 42.375rem;
    position: absolute;
    top: 0;
    left: 10.938rem;
    padding-top: 2.188rem;
  }

  .custom-height-img-basketball {
    max-height: 50.938rem;
    max-width: 61.938rem;
    position: absolute;
    top: unset;
    right: 7.813rem;
  }
}
@media screen and (min-width: 768px) and (max-width: 1919px) {
  .custom-height-img-athlete {
    max-height: 59.375rem;
    max-width: 42.375rem;
    position: absolute;
    left: 0;
    top: 6.563rem;
  }

  .custom-height-img-basketball {
    max-height: 35.5rem;
    max-width: 43.188rem;
    position: absolute;
    top: unset;
    right: 0;
  }
}
@media screen and (min-width: 320px) and (max-width: 767px) {
  .custom-height-img-athlete {
    max-height: 59.375rem;
    max-width: 42.375rem;
    position: relative;
    margin: 0 auto -5rem auto;
    z-index: 1;
  }

  .custom-height-img-basketball {
    position: relative;
    margin-bottom: -2.5rem;
    margin-top: 23px;
    margin-left: 0.5rem;
    z-index: 1;
  }
}
</style>
