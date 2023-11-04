<template>
  <div
    :class="
      isRight ? `content-players-items-${index}` : `content-items-${index}`
    "
    v-for="(item, index) in items"
    :key="index"
  >
    <div class="grid grid-cols-2 gap-0 container mx-auto">
      <div>&nbsp;</div>
      <div :class="isRight ? 'order-first' : 'md:-ml-[5rem]'">
        <div class="container-sub-title flex item-center">
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

<style lang="css" scoped>
.content-items-0 {
  background-color: #fff;
}
.content-items-1 {
  background-color: #f5f4f9;
}
.content-items-2 {
  background-color: #5e3db3;
}

.content-items-2 .number-underline {
  background-color: #fff;
}
.content-players-items-0 {
  background-color: #fff;
}
.content-players-items-1 {
  background-color: #f5f4f9;
}
.content-players-items-2 {
  background-color: #090c35;
}
.content-players-items-2 .text-number {
  color: #8f6be8;
}

.content-players-items-2 .number-underline {
  background-color: #fff;
}

.content-items-2 .text-content,
.content-players-items-2 .text-content {
  color: #fff;
}
</style>
