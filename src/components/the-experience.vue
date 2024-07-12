<script setup lang="ts">
import { TresCanvas } from '@tresjs/core'
import { OrbitControls } from '@tresjs/cientos'
</script>

<template>
  <!-- We need 4 core elements to create a 3D experience:
  1. A Scene to hold the camera and the object(s) together.
  2. A Renderer to render the scene into the DOM.
  3. A Camera
  4. An Object -->
  <!-- TresCanvas for Renderer and Scene -->
  <TresCanvas clear-color="#82DBC5" window-size>
    <!-- TresPerspectiveCamera for camera -->
    <TresPerspectiveCamera />
    <OrbitControls />

    <!-- TresMesh for Object -->
    <TresMesh>
      <TresTorusGeometry :args="[1, 0.5, 16, 32]" />
      <TresMeshBasicMaterial color="orange" />
    </TresMesh>
    <TresAmbientLight :intensity="1" />
  </TresCanvas>
</template>

<style>
html,
body,
#app {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
</style>
