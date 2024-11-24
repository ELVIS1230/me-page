<template>
  <section>

    <div class="card">
      <div class="flex gap-4 absolute bottom-4 left-4 ">
        <p class="bg-white p-1 text-black">Github</p>
        <p class="bg-white p-1 text-black">Github</p>
        <p class="bg-white p-1 text-black">Github</p>
      </div>
    </div>
  </section>

</template>

<script>
export default {
  name: 'CardProfile',
}
</script>

<style scoped>
* {
  --color: red;
}

.card {
  --color: #ff88a6;
  --border-size: 1rem;
  --bg-color: #5c5a5a;
  position: relative;
  background-color: var(--bg-color);
  width: 380px;
  height: 427px;
  margin: 5rem;
  border-radius: 1.5rem;
  display: grid;
  place-content: center;
  padding: 3rem 2rem;
  isolation: isolate;
  overflow: hidden;
}

.card::before,
.card::after {
  content: '';
  position: absolute;
}

.card::before {
  width: 200%;
  height: 200%;
  background-image: conic-gradient(#0dff79 0deg,
      transparent 60deg,
      transparent 180deg,
      #0dff79 180deg,
      transparent 240deg);
  inset: -50%;
  z-index: -2;
  animation: border 8s linear infinite;
}

@keyframes border {
  to {
    transform: rotateZ(-360deg);
  }

}

.card::after {
  --inset: 0.37rem;
  background-image: url('/person.jpeg');
  background-size: cover;
  inset: var(--inset);
  border: 1px solid black;
  border-radius: 1.2rem;
  z-index: -1;
  transition: all 0.35s linear;
}

.profile-image {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 16px;
}
</style>