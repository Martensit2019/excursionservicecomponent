<template>
  <div class="excursion__tag ml-1 mr-2" ref="tags">
    <v-icon v-if="tag.icon"> mdi-{{tag.icon}}</v-icon>
    {{ tag.title }}
  </div>
</template>

<script>
export default {
  props: {
    tag: {
      type: Object,
      default: () => {},
    },
  },

  mounted() {
    const currentHeight = `${this.$refs.tags.clientHeight}px`
    this.$emit('setHeight', currentHeight)
  },
}
</script>

<style lang="scss">
.excursion__tag {
  color: #888;
}
.excursion__tag + .excursion__tag {
  padding-left: 15px;
  position: relative;
  &::before {
    position: absolute;
    content: '';
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background-color: #000;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
  }
}
</style>
