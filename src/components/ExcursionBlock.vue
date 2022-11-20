<template>
  <div class="excursion__block">
    <h3 class="mb-4">Экскурсия в Янтарный</h3>
     <!-- Выравнивание по умолчанию: по ширине, в этом случае параметр alignment не задаём -->
    <excursion-tags :tags="tags" />
    <!-- Выравнивание по левому краю, в этом случае параметр alignment задаём и передаём left -->
    <!-- <excursion-tags :tags="tags" alignment="left" /> -->
  </div>
</template>

<script>
import ExcursionTags from './ExcursionTags.vue'
export default {
  components: { ExcursionTags },
  data() {
    return {
      tags: [
        {
          id: 1,
          icon: 'star-outline',
          title: 5,
        },
        {
          id: 2,
          icon: '',
          title: 'Историческая',
        },
        {
          id: 3,
          icon: 'bus',
          title: 'На автобусе',
        },
        {
          id: 4,
          icon: 'calendar-range',
          title: '28 марта',
        },
        {
          id: 5,
          icon: 'clock-outline',
          title: '9 часов',
        },
        {
          id: 6,
          icon: 'account',
          title: 'до 49',
        },
      ],
    }
  },
}
</script>

<style></style>
