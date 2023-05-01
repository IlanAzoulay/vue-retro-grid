<script>
import { defineComponent } from 'vue';
import VueRetroGrid from '@/vue-retro-grid.vue';

export default defineComponent({
  name: 'ServeDev',
  components: {
    VueRetroGrid
  }
});
</script>

<template>
  <div id="app">
    <vue-retro-grid 
      :update-interval="20"
      :frames-per-loop="8"
      :start-height="50"
      :amount-horizontals="15"
      :horizontal-factor-input="1.6"
      :amount-verticals="6"
      :vertical-angle-factor-input="1.6"
      :offset-vertical-lines-y="0.4"
      :offset-vertical-lines-x="1"
      :blurred-perspective="true"
      :grid-color="'blueviolet'"
      :background-color="'#24162F'"
    />
  </div>
</template>
