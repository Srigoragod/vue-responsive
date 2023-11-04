<template>
  <div class="grid grid-cols-2 gap-0 container mx-auto">
    <div></div>
    <div :class="title != 'athlets' ? 'order-first' : 'md:-ml-[5rem]'">
      <div class="header-title-h1 uppercase">
        {{ title }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopTitle",
  props: {
    title: String,
  },
};
</script>

<style lang="css" scoped></style>
