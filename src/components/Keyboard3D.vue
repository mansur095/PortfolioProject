<script setup lang="ts">
import { TresCanvas } from '@tresjs/core'
import { OrbitControls, GLTFModel } from '@tresjs/cientos' // только эти два реально нужны
</script>

<template>
  <TresCanvas
    style="width:700px; height:400px; background:transparent;"
  >
    <!-- камера и свет -->
    <TresPerspectiveCamera :position="[3, 2, 3]" />

    <!-- управление камерой -->
    <OrbitControls />

    <!-- базовый свет -->
    <TresAmbientLight :intensity="0.7" />
    <TresDirectionalLight :position="[2, 5, 2]" :intensity="1" />

    <!-- модель грузится асинхронно → через <Suspense> -->
    <Suspense>
      <GLTFModel path="/keyboard2.glb" :scale="0.3" />
      <template #fallback>
        Загрузка модели…
      </template>
    </Suspense>
  </TresCanvas>
</template>

<style scoped>
/* Если нужно, вынеси размеры/фон отсюда */
</style> 