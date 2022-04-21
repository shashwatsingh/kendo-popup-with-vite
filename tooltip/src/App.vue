<script lang="ts">
import { defineComponent } from "vue";
import "@progress/kendo-theme-bootstrap/dist/all.css";

import { Tooltip } from "@progress/kendo-vue-tooltip";

export default defineComponent({
  name: 'App',
  components: {
    "k-tooltip": Tooltip,
  },
})
</script>

<template>
  <main>
    <h1>Test Kendo with Vite: Tooltips</h1>

    <k-tooltip :openDelay="100" :position="'right'" :anchorElement="'target'">
      <span title="This is my tooltip">Hover over me</span>
    </k-tooltip>

  </main>
</template>
