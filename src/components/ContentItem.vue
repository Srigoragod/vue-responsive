<template>
  <div
    :class="
      isRight ? `content-players-items-${index}` : `content-items-${index}`
    "
    v-for="(item, index) in items"
    :key="index"
  >
    <div class="grid grid-cols-2 gap-0 container mx-auto">
      <div></div>
      <div :class="isRight ? 'order-first' : ' md:-ml-20'">
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
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContentItem",
  props: {
    items: { type: Array, required: false },
    isRight: { type: Boolean, default: false },
  },
};
</script>

<style lang="css">
@media screen and (min-width: 1919px) {
  .container {
    max-width: 1400px;
  }

  .content-items-0 .container {
    padding-top: 2.25rem;
    padding-bottom: 3.5rem;
  }
  .content-items-0 .container-sub-title {
    margin-bottom: 1.938rem;
  }
  #athlets .container-sub-title {
    margin-bottom: 1.313rem;
  }
  .content-items-1 {
    background: #f5f4f9;
  }
  .content-items-1 .container {
    padding-top: 3.313rem;
    padding-bottom: 3.5rem;
  }
  .content-items-2 {
    background: #5e3db3;
  }
  .content-items-2 .text-number {
    color: #000;
  }
  .content-items-2 .number-underline {
    background-color: #fff;
  }
  .content-items-2 .text-content {
    color: #fff;
  }

  .content-items-2 .container {
    padding-top: 5rem;
    padding-bottom: 6.125rem;
  }

  #players .number-underline {
    background-color: #603ebe;
  }
  .content-players-items-0 .container {
    padding-top: 4.25rem;
    padding-bottom: 4.313rem;
  }
  #players .container-sub-title {
    margin-bottom: 1.313rem;
  }
  .content-players-items-1 {
    background: #f5f4f9;
  }
  .content-players-items-1 .container {
    padding-top: 3.25rem;
    padding-bottom: 6.375rem;
  }
  .content-players-items-2 {
    background: #090c35;
  }
  #players .content-players-items-2 .number-underline {
    background-color: #fff;
  }
  .content-players-items-2 .text-number {
    color: #8f6be8;
  }
  .content-players-items-2 .text-content {
    color: #fff;
  }

  .content-players-items-2 .container {
    padding-top: 5.438rem;
    padding-bottom: 3.875rem;
  }
}

@media screen and (min-width: 768px) and (max-width: 1919px) {
  .content-items-0 .container {
    padding: 2.25rem 1.875rem 1.875rem 1.875rem;
  }

  #athlets .container-sub-title {
    margin-bottom: 1.313rem;
  }
  .content-items-1 {
    background: #f5f4f9;
  }
  .content-items-1 .container {
    padding: 1.875rem;
  }
  .content-items-2 {
    background: #5e3db3;
  }
  .content-items-2 .text-number {
    color: #000;
  }
  .content-items-2 .number-underline {
    background-color: #fff;
  }
  .content-items-2 .text-content {
    color: #fff;
  }

  .content-items-2 .container {
    padding: 1.875rem 1.875rem 3.625rem 1.875rem;
  }

  #players .number-underline {
    background-color: #603ebe;
  }
  #players .content-players-items-2 .number-underline {
    background-color: #fff;
  }
  .content-players-items-0 .container {
    padding: 2.125rem 1.875rem 0.625rem 1.875rem;
  }
  #players .container-sub-title {
    margin-bottom: 1.313rem;
  }
  .content-players-items-1 {
    background: #f5f4f9;
  }
  .content-players-items-1 .container {
    padding: 2.125rem 1.875rem 0.625rem 1.875rem;
  }
  .content-players-items-2 {
    background: #090c35;
  }
  .content-players-items-2 .text-number {
    color: #8f6be8;
  }

  .content-players-items-2 .text-content {
    color: #fff;
  }

  .content-players-items-2 .container {
    padding-top: 2.75rem;
    padding-bottom: 4.5rem;
    padding-left: 1.875rem;
    padding-right: 1.875rem;
  }
  /* .container {
  max-width: 720px;
} */
  .text-content {
    color: #000;
    font-size: 1.125rem;
    line-height: 1.75rem;
    width: 27rem;
  }
}

@media screen and (min-width: 320px) and (max-width: 767px) {
  .grid-cols-2 {
    display: grid;
    grid-template-columns: repeat(1, minmax(0, 1fr));
    margin: auto 1.125rem;
  }
  .div-image-mobile {
    margin-top: 0.688rem;
  }
  .text-number {
    font-size: 0.875rem;
    padding-bottom: 0.125rem;
  }
  .title-h3 {
    font-size: 1.75rem;
    padding-top: 0;
  }

  .content-items-0 .container {
    padding: 0;
  }

  #athlets .container-sub-title {
    margin-bottom: 1.313rem;
  }
  .content-items-0,
  .content-items-1,
  .content-items-2 {
    padding: 4.5rem 0 4.313rem 0;
    background: #f5f4f9;
  }

  .content-items-2 .container {
    padding: 1.875rem 0 3.625rem 0;
  }

  #players .header-title-h1 {
    padding-bottom: 1.438rem;
    font-size: 3.125rem;
  }
  #players .number-underline {
    background-color: #603ebe;
  }
  #players .content-players-items-2 .number-underline {
    background-color: #fff;
  }
  .content-players-items-0 .container {
    padding: 0;
  }
  #players .container-sub-title {
    margin-bottom: 1.313rem;
  }
  .content-players-items-1 {
    background: #f5f4f9;
  }
  .content-players-items-1 .container {
    padding-top: 3.188rem;
    padding-bottom: 4.063rem;
  }
  .content-players-items-2 {
    background: #090c35;
  }
  .content-players-items-2 .text-number {
    color: #8f6be8;
  }

  .content-players-items-2 .text-content {
    color: #fff;
  }

  .content-players-items-2 .container {
    padding-top: 2.75rem;
    padding-bottom: 4.5rem;
  }
  .text-content {
    color: #000;
    font-size: 0.938rem;
    line-height: normal;
    padding: 1.25rem 0 1.25rem 0;
  }
}
</style>
