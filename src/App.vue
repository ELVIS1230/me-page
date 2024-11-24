<template>
  <div class=" h-screen m-0">
    <div class="h-screen flex">
      <div class="grid grid-cols-2">
        <div class="ml-36 flex flex-col justify-center w-auto">
          <p class="text-5xl">Full Stack Developer and Movil</p>
          <p class="font-extrabold text-[150px] text-[#0dff79]">I'm Elvis</p>
          <div class="flex gap-96  pr-10">
            <p class="mt-4">
              Lorem Ipsum is simply dummy text of the printing and typesetting industry.
              Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took
              a
              galley of type and scrambled it to make a type specimen b Ipsum.
            </p>
          </div>
          <div class="mt-10 flex gap-20 justify-center items-center">
            <p class="font-bold text-xl cursor-pointer duration-500 hover:text-[#0dff79] hover:-translate-y-2">EXPERIENCE</p>
            <p class="font-bold text-xl cursor-pointer duration-500 hover:text-[#0dff79] hover:-translate-y-2">ESTUDIES</p>
            <p class="font-bold text-xl cursor-pointer duration-500 hover:text-[#0dff79] hover:-translate-y-2">CONTACTS</p>
          </div>
        </div>
        <div class="flex items-center justify-center gap-4 ">
          <CardProfile />
        </div>
      </div>
      <!-- <div class="w-64 vertical-text flex gap-20 flex-col  justify-center">
        <p class="text font-bold text-xl">EXPERIENCE</p>
        <p class="text font-bold text-xl">ESTUDIES</p>
        <p class="text font-bold text-xl">CONTACTS</p>
      </div> -->
    </div>
    <div class="border-2 border-black h-screen flex items-center justify-center">
        <p class="text-5xl font-bold">Experiencia laboral</p> 
    </div>
    <div class="border-2 border-black h-screen flex items-center justify-center">
        <p class="text-5xl font-bold">Estudies</p> 
    </div>
    <div class="border-2 border-black h-screen flex items-center justify-center">
        <p class="text-5xl font-bold">Contacts</p> 
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
