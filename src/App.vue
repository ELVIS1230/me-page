<template>
  <div class=" h-screen m-0">
    <!-- <div class="h-screen flex">
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
              <font-awesome-icon :icon="['fab', 'github']" />
            </p>
          </div>
          <div class="mt-10 flex gap-20 justify-center items-center">
            <p class="font-bold text-xl p-2 cursor-pointer duration-500 hover:text-[#0dff79] hover:-translate-y-2">
              EXPERIENCE</p>
            <p class="font-bold text-xl p-2 cursor-pointer duration-500 hover:text-[#0dff79] hover:-translate-y-2">
              ESTUDIES</p>
            <p class="font-bold text-xl p-2 cursor-pointer duration-500 hover:text-[#0dff79] hover:-translate-y-2">
              CONTACTS</p>
          </div>
        </div>
        <div class="flex items-center justify-center gap-4 ">
          <CardProfile />
        </div>
      </div>
    </div> -->
    <div class="h-screen flex">
      <div class="flex ">
        <div class="  flex flex-col w-6/12">
          <div class="border-2 px-10 flex gap-10 items-center bg-white/90 backdrop-blur-sm rounded-ee-full">
            <img src="./public/logo_loog_black.png" alt="Profile Image" class="h-16 object-cover " />
            <div class="flex gap-4 text-black font-semibold text-lg">
              <div v-for="item in navbar" :key="item.value" class="px-4 text-sm py-2 rounded-xl hover:cursor-pointer"
                :class="{ 'bg-[#0dff79]  ': activeSection == item.value }">
                <span>{{ item.name }}</span>
              </div>
            </div>
          </div>
          <div class="pl-20">
            <div>
              <p class="font-extrabold text-8xl mt-36 text-[#0dff79]">Elvis Gomez</p>
              <p class="text-3xl">Full Stack Developer & Movil</p>
              <div class="h-1 bg-white w-7/12 mt-6 rounded-md" />
            </div>
            <div class="mt-24 w-9/12">
              <p>
                Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
                industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and
                scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap
                into
                electronic typesetting, remaining essentially unchanged.
              </p>
            </div>
          </div>
        </div>
        <div class="flex justify-between w-7/12 ">
          <div class="relative h-screen ">
            <img src="./public/avatar_bg.png" alt="Profile Image" class="w-full h-full object-cover" />
            <div
              class="absolute top-24 left-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-[#0dff79] bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">About me</p>
            </div>
            <div
              class="absolute top-24 right-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-[#0dff79] bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">Experience</p>
            </div>
            <div
              class="absolute bottom-72 left-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-[#0dff79] bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">Education</p>
            </div>
            <div
              class="absolute bottom-72 right-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-[#0dff79] bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">Contacts</p>
            </div>
          </div>
          <div class="flex flex-col ">
            <div class="flex items-center flex-col justify-center gap-4  px-6  h-[95%]">
              <p>01</p>
              <div v-for="section in navbar" :key="section.value" @click="activeSection = section.value">
                <div v-if="activeSection === section.value"
                  class="w-8 h-8 rounded-full flex items-center justify-center  border-2 border-[#0dff79]">
                  <div class="w-3 h-3 rounded-full bg-[#0dff79]"></div>
                </div>
                <div v-else class="w-3 h-3 rounded-full border-2 border-[#0dff79] "></div>
              </div>
              <p>04</p>
            </div>
            <div class="w-24 h-24 ">
              <img src="./public/isotipo_loog_white.png" alt="Profile Image" class="w-full h-full object-cover" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="border-2 border-black h-screen grid grid-cols-2 place-items-center">
      <p class="text-5xl font-bold">Experiencia laboral</p>
      <div class="flex h-4/5 w-full items-center justify-center p-6">
        <div class="grid h-full w-full grid-cols-10 grid-rows-4 gap-4">
          <div class=" col-span-4 row-span-3 bg-[#0dff79] rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-3 xl:col-span-4 row-span-1 bg-indigo-300 rounded-3xl flex justify-center items-center">
          </div>
          <div class=" col-span-3 xl:col-span-2 row-span-1 bg-indigo-300 rounded-3xl flex justify-center items-center">
          </div>
          <div class=" col-span-3 row-span-2 bg-indigo-300 rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-3 row-span-2 bg-indigo-300 rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-4 row-span-1 bg-[#0dff79] rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-6 row-span-1 bg-[#0dff79] rounded-3xl flex justify-center items-center"></div>
        </div>
      </div>
    </div>
    <div class="border-2 border-black h-screen flex flex-col items-center justify-center p-4">
      <p class="text-5xl font-bold">Education</p>
      <div class="border-2 border-white w-full h-full grid grid-cols-2">
        <div class=" border-2 border-red-500 flex flex-col items-center">
          <p class="text-5xl font-bold text-center text-[#0dff79]">Estudies</p>
          <div class="border-l-2 border-[#0dff79] px-2 flex flex-col gap-6 ">
            <div class="border-2 border-red-500">
              <p class="text-[#0dff79]">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
            <div>
              <p class="text-[#0dff79]">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
            <div>
              <p class="text-[#0dff79]">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
            <div>
              <p class="text-[#0dff79]">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
          </div>
        </div>
        <div class=" border-2 border-red-500 flex flex-col items-center">
          <p class="text-5xl font-bold text-center text-[#0dff79]">Stack</p>
          <div class="grid grid-cols-3 gap-4 mt-4">
            <div class="h-32 w-32 bg-[#0dff79] rounded-md flex items-center justify-center">
              <p class="text-white">HTML</p>
            </div>
            <div class="h-32 w-32 bg-[#0dff79] rounded-md flex items-center justify-center">
              <p class="text-white">CSS</p>
            </div>
            <div class="h-32 w-32 bg-[#0dff79] rounded-md flex items-center justify-center">
              <p class="text-white">JavaScript</p>
            </div>
          </div>

          <p class="text-5xl font-bold text-center text-[#0dff79]">Technologies</p>
          <div class="grid grid-cols-3 gap-4 mt-4">
            <div class="h-32 w-32 bg-[#0dff79] rounded-md flex items-center justify-center">
              <p class="text-white">HTML</p>
            </div>
            <div class="h-32 w-32 bg-[#0dff79] rounded-md flex items-center justify-center">
              <p class="text-white">CSS</p>
            </div>
            <div class="h-32 w-32 bg-[#0dff79] rounded-md flex items-center justify-center">
              <p class="text-white">JavaScript</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="border-2 border-black h-screen flex items-center justify-center">
      <p class="text-5xl font-bold">Contacts</p>
    </div>
  </div>
</template>
<script lang="ts">
import CardProfile from './components/CardProfile.vue';

export default {
  components: { CardProfile },
  data() {
    return {
      activeSection: 'experience',
      navbar: [
        { name: 'About me', link: '#about', value: 'home' },
        { name: 'Experience', link: '#experience', value: 'experience' },
        { name: 'Studies', link: '#studies', value: 'studies' },
        { name: 'Contacts', link: '#contacts', value: 'contacts' },
      ]
    }
  }
}
</script>
<style scoped>
.text {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
}
</style>
