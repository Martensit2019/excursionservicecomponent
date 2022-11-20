<template>
  <div class="d-flex mb-3 flex-wrap overflow-y-hidden" :class="alignment ? 'justify-start' : 'justify-space-between'" ref="tags">
    <excursion-tag v-for="tag in tags" :tag="tag" :key="tag.id" @setHeight="setHeight" />
  </div>
</template>

<script>
import ExcursionTag from './ExcursionTag.vue'
export default {
  components: { ExcursionTag },
  props: {
    tags: {
      type: Array,
      default: () => [],
    },
    alignment: {
      type: String,
      default: '',
    },
  },
  methods: {
    setHeight(height) {
      this.$refs.tags.style.maxHeight = height
    },
  },
}
</script>
