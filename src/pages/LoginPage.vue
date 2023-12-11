<template>
  <div class="column flex flex-center window-height bg-black text-white q-gutter-y-md">
    <img :src="Logo" />
    <span class="text-h5">Login to OWL</span>
    <q-form class="column q-gutter-y-md" style="width: 30%">
      <q-input label="Username" standout="bg-tranparent text-grey-1" color="grey-1" label-color="grey-1"/>
      <q-input label="Password" standout="bg-tranparent text-grey-1" color="grey-1" label-color="grey-1" type="password" >
        <template v-slot:append>
          <q-icon name="mdi-eye" />
        </template>
      </q-input>
      <div class="self-end column">
        <router-link to="/forgot_password">Forgot Password?</router-link>
        <q-btn color="blue-7" label="Login" no-caps />
      </div>
    </q-form>
  </div>
</template>

<script setup lang="ts">
import { defineComponent } from 'vue'
import Logo from 'src/assets/logo.png';

defineComponent({
  name: 'LoginPage'
})
</script>
