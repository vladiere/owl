<template>
  <q-page padding>
    <q-tabs
      v-model="tab"
      dense
      class="text-grey"
      active-color="primary"
      indicator-color="primary"
      align="justify"
      narrow-indicator
    >
      <q-tab name="peoplelist" label="List of People" />
      <q-tab name="peopleadd" label="Add People" />
    </q-tabs>
  </q-page>
</template>

<script setup lang="ts">
import { defineComponent, ref } from 'vue'

defineComponent({
  name: 'AccountsPage'
});

const tab = ref('peoplelist');
</script>
