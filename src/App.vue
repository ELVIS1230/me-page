<template>
  <div class=" h-screen m-0">
    <div class="h-screen flex">
      <div class="mt-44 ml-48">
        <p class="text-5xl">Hello web,</p>
        <h1 class="font-extrabold text-[175px]">I'm Elvis</h1>
        <div class="flex gap-96 w-11/12 pr-10">
          <p class="w-1/3">
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a
            galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but
            also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s
            with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing
            software like Aldus PageMaker including versions of Lorem Ipsum.
          </p>
          <div class="flex flex-col mt-16 gap-4">
            <p class="text-xl">Aquí va un texto para explicar algo</p>
            <p class="text-xl">Aquí otro texto va un texto y aquí también</p>

          </div>
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

<style scoped>
.text {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
}
</style>
