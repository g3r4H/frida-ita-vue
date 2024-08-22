<template>
  <div class="flex h-full flex-col gap-2 border-2 border-red-500">
    <section class="flex-none border-2 border-green-500">
      <div class="flex w-full flex-nowrap justify-between">
        <coe-card name="Notify me" counter="5"> </coe-card>
        <coe-card name="Notify me" counter="8"> </coe-card>
        <coe-card name="Notify me" counter="0"> </coe-card>
      </div>
    </section>
    <section class="flex-1 border-2 border-blue-500">
      Content
      <section class="sidebar">
        <coe-sidemenu></coe-sidemenu>
      </section>
      <main>
        <section class="notifications"></section>
        <section class="stepper"></section>
        <section class="boxes"></section>
      </main>
    </section>
  </div>
</template>

<script lang="ts">
import 'coe-comp-lib'
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
