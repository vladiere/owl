<template>
  <q-layout view="lHh LpR fFf">

    <q-header elevated class="bg-black text-white">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <!-- <q-toolbar-title> -->
        <!--   <q-avatar> -->
        <!--     <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg"> -->
        <!--   </q-avatar> -->
        <!--   Title -->
        <!-- </q-toolbar-title> -->
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered class="bg-black text-white">
      <q-item-label header class="text-h3 row items-center justify-around">
        <q-avatar rounded>
          <q-img src="src/assets/logo.png" />
        </q-avatar>
        OWL
      </q-item-label>

      <q-list bordered>
          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon size="3em" color="white" name="mdi-home" />
            </q-item-section>

            <q-item-section>Dashboard</q-item-section>
          </q-item>

          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon size="3em" color="white" name="mdi-key-variant" class="rotate-45" />
            </q-item-section>

            <q-item-section>Accounts</q-item-section>
          </q-item>

          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon size="3em" color="white" name="mdi-history" />
            </q-item-section>

            <q-item-section>RT Monitoring</q-item-section>
          </q-item>

          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon size="3em" color="white" name="mdi-file-chart" />
            </q-item-section>

            <q-item-section>Report</q-item-section>
          </q-item>

      </q-list>
    </q-drawer>

    <q-page-container class="text-white">
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const leftDrawerOpen = ref(false)

const toggleLeftDrawer = () => {
   leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
