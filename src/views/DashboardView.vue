<template>
  <div class="flex h-full flex-col gap-2">
    <!-- Navigation -->
    <section class="flex-none">
      <p class="text-center">Navigation</p>
    </section>

    <!-- Page Content -->
    <section class="flex flex-1 flex-nowrap gap-2">
      <!-- Left Side -->
      <section class="flex-none rounded-md border-2 border-gray-300 p-2">
        <!-- Side menu -->
        <section class="rounded-md">
          <coe-sidemenu></coe-sidemenu>
        </section>
      </section>

      <!-- Right Side -->
      <main class="flex flex-1 flex-col gap-2">
        <!-- Notifications -->
        <section
          class="flex flex-nowrap justify-center gap-2 rounded-md border-2 border-gray-300 p-4"
        >
          <coe-card name="Notify me" counter="5"></coe-card>
          <coe-card name="Notify me" counter="8"></coe-card>
          <coe-card name="Notify me" counter="0"></coe-card>
          <coe-card name="Notify me" counter="0"></coe-card>
          <coe-card name="Notify me" counter="0"></coe-card>
          <coe-card name="Notify me" counter="0"></coe-card>
          <coe-card name="Notify me" counter="0"></coe-card>
        </section>

        <!-- Stepper -->
        <section class="rounded-md border-2 border-gray-300">
          <p class="text-center">Stepper</p>
        </section>

        <!-- Boxes -->
        <section class="flex h-full flex-col gap-2 rounded-md border-2 border-gray-300 p-4">
          <section class="flex-1 content-center justify-center border-2 border-gray-300">
            <div class="text-center">Box 1</div>
          </section>
          <section class="flex-1 content-center justify-center border-2 border-gray-300">
            <div class="text-center">Box 2</div>
          </section>
        </section>
      </main>
    </section>
  </div>
</template>

<script lang="ts">
import 'coe-comp-lib'

export default {}
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
