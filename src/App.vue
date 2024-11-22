<template>
  <div class=" h-screen m-0">
    <div class="h-screen flex">
      <div class="mt-44 grid grid-cols-2">
        <div class="ml-36 border-2 border-red-500 w-auto">
          <p class="text-5xl">Hello web,</p>
          <h1 class="font-extrabold text-[175px]">I'm Elvis</h1>
          <div class="flex gap-96  pr-10">
            <p class="w-2/3">
              Lorem Ipsum is simply dummy text of the printing and typesetting industry.
              Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took
              a
              galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but
              also the leap into electronic typesetting, remaining essentially unchanged. It was popularized in the
              1960s
              with the release of Legraste sheets containing Lorem Ipsum passages, and more recently with desktop
              publishing
              software like Lauds PageMaker including versions of Lorem Ipsum.
            </p>
          </div>
        </div>
        <div class="flex items-center justify-center gap-4 border-2 border-blue-500">
          <CardProfile />
        </div>
      </div>
      <div class="w-64 vertical-text flex gap-20 flex-col  justify-center">
        <p class="text font-bold text-xl">EXPERIENCE</p>
        <p class="text font-bold text-xl">ESTUDIES</p>
        <p class="text font-bold text-xl">CONTACTS</p>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import CardProfile from './components/CardProfile.vue';

export default {
  components: { CardProfile }
}
</script>
<style scoped>
.text {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
}
</style>
