<template>
  <div class="grid grid-cols-2 gap-0 container mx-auto">
    <div></div>
    <div :class="title != 'athlets' ? 'order-first' : 'md:-ml-20'">
      <div class="header-title-h1 text-uppercase">
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

<style lang="css" scoped>
.header-title-h1 {
  color: #e7e7e7;
  font-size: 5.625rem;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
@media screen and (min-width: 1920px) {
  #athlets .header-title-h1 {
    padding-top: 1.5rem;
  }
  #players .header-title-h1 {
    padding-top: 7.75rem;
  }
}

@media screen and (min-width: 768px) and (max-width: 1919px) {
  #athlets .header-title-h1 {
    padding-top: 5.438rem;
  }
  #players .header-title-h1 {
    padding-top: 3.25rem;
    padding-left: 1.875rem;
  }
}
@media screen and (min-width: 320px) and (max-width: 767px) {
  .athlets .header-title-h1 {
    font-size: 3.125rem;
    position: relative;
    margin-left: 1.125rem;
  }
  .players .header-title-h1 {
    margin-top: 1.188rem;
    margin-left: 1.125rem;
  }
}
</style>
