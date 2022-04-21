<script lang="ts">
import { defineComponent, reactive } from "vue";
import "@progress/kendo-theme-bootstrap/dist/all.css";

import {
  DropDownList,
  DropDownListChangeEvent,
} from "@progress/kendo-vue-dropdowns";

export default defineComponent({
  name: 'App',
  components: {
    "k-dropdown": DropDownList,
  },
  setup() {
    const items = reactive([
      {
        ID: 100,
        Name: 'Jill',
      },
      {
        ID: 200,
        Name: "Jack",
      }
    ]);
    const changed = (e: DropDownListChangeEvent) => console.log('changed', e);

    return {
      items,
      changed
    }
  }
})
</script>

<template>
  <main>
    <h1>Test Kendo with Vite: DropDownList</h1>

    <k-dropdown class="form-control" :data-items="items" :text-field="'Name'" :value-field="'ID'" @change="changed" />
  </main>
</template>
