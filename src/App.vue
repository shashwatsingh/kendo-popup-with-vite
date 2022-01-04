<script lang="ts">

import { Popup } from '@progress/kendo-vue-popup';
import { defineComponent } from 'vue';

export default defineComponent({
  components: {
    'k-popup': Popup,
  },
  data() {
    return {
      show: false,
    }
  },
  methods: {
    onClick() {
      this.show = !this.show;
    }
  }
});

</script>

<template>
  <div>
    <button class="k-button" @click="onClick" ref="buttonWithPopup">Click Me</button>
    <k-popup :anchor="'buttonWithPopup'" :show="show">Popup content.</k-popup>
  </div>
</template>
