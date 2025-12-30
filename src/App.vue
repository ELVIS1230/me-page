<template>
  <div class="scroll-smooth h-screen overflow-y-auto snap-y snap-mandatory scroll-hidden">
    <div
      class="absolute top-0 left-0 z-50 border-2 px-4 md:px-10 flex gap-4 md:gap-10 items-center bg-white/90 backdrop-blur-sm rounded-ee-full">
      <img src="./public/logo_loog_black.png" alt="Profile Image" class="h-12 md:h-16 object-cover" />
      <div class="flex gap-2 md:gap-4 text-black font-semibold text-sm md:text-lg">
        <div v-for="item in navbar" :key="item.value" @click="scrollToSection(item.value)"
          class="px-2 md:px-4 text-xs md:text-sm py-2 rounded-xl hover:cursor-pointer transition-all duration-500 ease-in-out delay-150"
          :class="{ 'bg-primary': activeSection == item.value }">
          <span>{{ item.name }}</span>
        </div>
      </div>
    </div>
    <div class="absolute h-screen right-0 hidden lg:flex flex-col overflow-hidden w-full lg:w-3/12 items-stretch">
      <div class="relative h-[20rem] w-full">
        <img src="./public/olas-line.png"
          class="absolute scale-[1.5] lg:scale-[2] -right-20 lg:-right-44  lg:-top-96 rotate-[20deg] z-0 opacity-30" />
      </div>
      <div class="w-1/4 flex flex-col items-center flex-1 justify-between self-end">
        <div
          class="flex items-center flex-col justify-center gap-4 w-fit bg-white/10 backdrop-blur-md border border-white/20 shadow-lg rounded-3xl px-2 py-8 ">
          <p class="text-white font-semibold text-sm">01</p>
          <div v-for="section in navbar" :key="section.value" @click="scrollToSection(section.value)"
            class="cursor-pointer transition-all duration-500 ease-in-out delay-150">
            <div
              v-show="activeSection === section.value"
              class="w-8 h-8 rounded-full flex items-center justify-center border-2 border-primary bg-primary/20 transition-all duration-500 ease-in-out delay-500">
              <div class="w-3 h-3 rounded-full bg-primary transition-all duration-500 ease-in-out delay-500"></div>
            </div>
            <div
              v-show="activeSection !== section.value"
              class="w-3 h-3 rounded-full border-2 border-white/60 hover:border-white transition-all duration-500 ease-in-out delay-150">
            </div>
          </div>
          <p class="text-white font-semibold text-sm">04</p>
        </div>
        <div class="w-16 h-16 lg:w-24 lg:h-24 self-end">
          <img src="./public/isotipo_loog_white.png" alt="Profile Image" class="w-full h-full object-cover " />
        </div>
      </div>
    </div>
    <div id="home" class="h-screen flex w-full snap-start">
      <div class="flex w-full flex-col lg:flex-row overflow-hidden">
        <!-- Navbar -->

        <!-- Main Content -->
        <div class="flex flex-col lg:flex-row w-full mt-20 lg:mt-0">
          <!-- Left Section - Text -->
          <div class="w-full lg:w-3/12 grid grid-cols-1 grid-rows-2 items-stretch relative z-10 justify-center">
            <div class="w-full flex items-end pb-6 lg:pb-12 lg:ml-14 ">
              <div>
                <p class="text-sm md:text-xl font-light">Full Stack Developer & Movil</p>
                <p class="font-bold text-4xl leading-none md:text-[4rem]   text-primary">Elvis Gomez</p>
                <div class="h-0.5 bg-white w-7/12 mt-4 rounded-md" />
              </div>
            </div>
            <div class="relative overflow-hidden hidden lg:block ">
              <img src="./public/olas-line.png"
                class="absolute scale-[1.5] lg:scale-[2] rotate-[20deg] -left-40 lg:-left-72 -bottom-40 lg:-bottom-60 z-0 opacity-30" />
            </div>
          </div>

          <!-- Center Section - Avatar -->
          <div class="relative w-full lg:w-6/12  flex items-center justify-center">
            <div
              class="w-64 h-64 sm:w-80 sm:h-80 md:w-96 md:h-96 lg:w-[36rem] lg:h-[36rem] bg-primary rounded-full absolute top-5 lg:top-10 left-1/2 -translate-x-1/2 z-0 neon-circle">
            </div>
            <div class="w-10/12 lg:w-10/12 m-auto pl-4 relative z-10">
              <img src="./public/avatar_bg.png" alt="Profile Image" class="relative w-full h-full object-cover z-10" />
            </div>
          </div>

          <!-- Right Section - Navigation Dots -->

        </div>
        <!-- <img src="./public/olas.svg" alt="Decorative Lines" /> -->
        <!-- <div class="pl-20">
            <div>
              <p class="font-extrabold text-8xl mt-36 text-primary">Elvis Gomez</p>
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
          </div> -->
      </div>
      <!-- <div class="flex justify-between w-7/12 ">
          <div class="relative h-screen ">
            <div class="w-[36rem] h-[36rem] bg-primary border-2 rounded-full absolute top-10 left-1/2 -translate-x-1/2 z-0 neon-circle"></div>

            <img src="./public/avatar_bg.png" alt="Profile Image" class="relative border-2 w-full h-full left-1/2 -translate-x-1/2 object-cover z-10" />
            <div
              class="absolute top-24 left-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-primary bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">About me</p>
            </div>
            <div
              class="absolute top-24 right-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-primary bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">Experience</p>
            </div>
            <div
              class="absolute bottom-72 left-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-primary bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">Education</p>
            </div>
            <div
              class="absolute bottom-72 right-6 rounded-md hover:cursor-pointer hover:-translate-y-2 duration-500 border-2 hover:border-primary bg-gray-200/35 backdrop-blur-0 px-4 py-2 text-sm font-medium text-white shadow-sm ">
              <p class="font-bold">Contacts</p>
            </div>
          </div>
          <div class="flex flex-col ">
            <div class="flex items-center flex-col justify-center gap-4  px-6  h-[95%]">
              <p>01</p>
              <div v-for="section in navbar" :key="section.value" @click="activeSection = section.value">
                <div v-if="activeSection === section.value"
                  class="w-8 h-8 rounded-full flex items-center justify-center  border-2 border-primary">
                  <div class="w-3 h-3 rounded-full bg-"></div>
                </div>
                <div v-else class="w-3 h-3 rounded-full border-2 border-primary "></div>
              </div>
              <p>04</p>
            </div>
            <div class="w-24 h-24 ">
              <img src="./public/isotipo_loog_white.png" alt="Profile Image" class="w-full h-full object-cover" />
            </div>
          </div>
        </div> -->
    </div>
    <div id="experience" class="border-2 border-black h-screen grid grid-cols-2 place-items-center snap-start">
      <p class="text-5xl font-bold">Experiencia laboral</p>
      <div class="flex h-4/5 w-full items-center justify-center p-6">
        <div class="grid h-full w-full grid-cols-10 grid-rows-4 gap-4">
          <div class=" col-span-4 row-span-3 bg-primary rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-3 xl:col-span-4 row-span-1 bg-indigo-300 rounded-3xl flex justify-center items-center">
          </div>
          <div class=" col-span-3 xl:col-span-2 row-span-1 bg-indigo-300 rounded-3xl flex justify-center items-center">
          </div>
          <div class=" col-span-3 row-span-2 bg-indigo-300 rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-3 row-span-2 bg-indigo-300 rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-4 row-span-1 bg-primary rounded-3xl flex justify-center items-center"></div>
          <div class=" col-span-6 row-span-1 bg-primary rounded-3xl flex justify-center items-center"></div>
        </div>
      </div>
    </div>
    <div id="studies" class="border-2 border-black h-screen flex flex-col items-center justify-center p-4 snap-start">
      <p class="text-5xl font-bold">Education</p>
      <div class="border-2 border-white w-full h-full grid grid-cols-2">
        <div class=" border-2 border-red-500 flex flex-col items-center">
          <p class="text-5xl font-bold text-center text-">Estudies</p>
          <div class="border-l-2 border-primary px-2 flex flex-col gap-6 ">
            <div class="border-2 border-red-500">
              <p class="text-">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
            <div>
              <p class="text-">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
            <div>
              <p class="text-">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
            <div>
              <p class="text-">2020-2025</p>
              <p>Bachillerato tecnico </p>
              <p>Conocimiento en desarrollo web asdasdsdasdsad</p>
            </div>
          </div>
        </div>
        <div class=" border-2 border-red-500 flex flex-col items-center">
          <p class="text-5xl font-bold text-center text-">Stack</p>
          <div class="grid grid-cols-3 gap-4 mt-4">
            <div class="h-32 w-32 bg- rounded-md flex items-center justify-center">
              <p class="text-white">HTML</p>
            </div>
            <div class="h-32 w-32 bg- rounded-md flex items-center justify-center">
              <p class="text-white">CSS</p>
            </div>
            <div class="h-32 w-32 bg- rounded-md flex items-center justify-center">
              <p class="text-white">JavaScript</p>
            </div>
          </div>

          <p class="text-5xl font-bold text-center text-">Technologies</p>
          <div class="grid grid-cols-3 gap-4 mt-4">
            <div class="h-32 w-32 bg- rounded-md flex items-center justify-center">
              <p class="text-white">HTML</p>
            </div>
            <div class="h-32 w-32 bg- rounded-md flex items-center justify-center">
              <p class="text-white">CSS</p>
            </div>
            <div class="h-32 w-32 bg- rounded-md flex items-center justify-center">
              <p class="text-white">JavaScript</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id="contacts" class="border-2 border-black h-screen flex items-center justify-center snap-start">
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
      activeSection: 'home',
      navbar: [
        { name: 'About me', link: '#about', value: 'home' },
        { name: 'Experience', link: '#experience', value: 'experience' },
        { name: 'Studies', link: '#studies', value: 'studies' },
        { name: 'Contacts', link: '#contacts', value: 'contacts' },
      ],
      observer: null as IntersectionObserver | null
    }
  },
  mounted() {
    this.setupScrollListener();
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    scrollToSection(sectionId: string) {
      console.log('Scrolling to section:', sectionId);
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth', block: 'start' });
        this.activeSection = sectionId;
      }
    },
    handleScroll() {
      const scrollContainer = document.querySelector('.scroll-hidden') as HTMLElement;
      if (!scrollContainer) return;
      console.log('Scroll event detected');
      const scrollTop = scrollContainer.scrollTop;
      const viewportHeight = scrollContainer.clientHeight;
      const viewportCenter = scrollTop + viewportHeight / 2;
      const sections = ['home', 'experience', 'studies', 'contacts'];

      let maxVisibleArea = 0;
      let activeSectionId = 'home';

      for (const sectionId of sections) {
        const element = document.getElementById(sectionId);
        if (element) {
          const { offsetTop, offsetHeight } = element;
          const sectionTop = offsetTop;
          const sectionBottom = offsetTop + offsetHeight;

          // Calcular cuánto de la sección es visible en el viewport
          const visibleTop = Math.max(sectionTop, scrollTop);
          const visibleBottom = Math.min(sectionBottom, scrollTop + viewportHeight);
          const visibleArea = Math.max(0, visibleBottom - visibleTop);

          // Usar la sección que tiene más área visible
          if (visibleArea > maxVisibleArea) {
            maxVisibleArea = visibleArea;
            activeSectionId = sectionId;
          }
        }
      }

      if (this.activeSection !== activeSectionId) {
        this.activeSection = activeSectionId;
      }
    },
    setupScrollListener() {
      const scrollContainer = document.querySelector('.scroll-hidden') as HTMLElement;
      if (scrollContainer) {
        scrollContainer.addEventListener('scroll', this.handleScroll.bind(this));
      }
    }
  }
}
</script>
<style scoped>
.text {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
}

.neon-circle {
  box-shadow: 0 0 30px rgba(59, 130, 246, 1), 0 0 60px rgba(59, 130, 246, 0.8), 0 0 90px rgba(59, 130, 246, 0.6), inset 0 0 30px rgba(59, 130, 246, 0.5);
  border-color: rgba(59, 130, 246, 1);
}

.scroll-hidden::-webkit-scrollbar {
  display: none;
}

.scroll-hidden {
  -ms-overflow-style: none;
  scrollbar-width: none;
}
</style>
