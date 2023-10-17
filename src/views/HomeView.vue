<template>
  <div>
    <div class="flex h-screen justify-center items-center">
      <div class="">
        <main class="flex flex-col lg:flex-row items-center">
          <div>
            <p class="dark:text-green-400 text-xl">Hi, my name is</p>
            <h1 class="big-title">
              <span class="font-bold underline decoration-green-400">Sam</span>
              Nmeje.
            </h1>
            <h1 class="text-5xl text-slate-200 font-bold">
              I build things for

              <transition name="slide-fade" @after-leave="changeText">
                <p class="text-2xl" v-show="showText">{{ currentText }}</p>
              </transition>
            </h1>
            <p class="text-justify py-4 regular-text">
              I'm a seasoned Software Engineer based in Scotland, with expertise
              in creating captivating digital experiences. Leveraging modern web
              development tools like Vue and React, I craft functional and
              intuitive interfaces that captivate users. Passionate about
              continuous learning, I'm always on the lookout for emerging web
              technologies to further elevate website and online application
              design and usability.
            </p>
          </div>
        </main>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
const texts = ref([
  "... the Web. Where dreams meet screens.",
  ".... Businesses. Turning visions into ventures.",
  "...Everyone. Crafting pixels for the people..",
]);
const currentText = ref(texts.value[0]);

const showText = ref(true);

const changeText = () => {
  const index = texts.value.indexOf(currentText.value);
  currentText.value = texts.value[index + 1] || texts.value[0];
  showText.value = true; // Show the text after changing it
};

const startTransition = () => {
  showText.value = false;
};

onMounted(() => {
  setInterval(() => {
    startTransition();
  }, 4000);
});
</script>

<style scoped>
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: transform 1s;
  transform-style: preserve-3d;
  perspective: 1000px;
}

/* For slide-in */
.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: rotateX(90deg);
  opacity: 0;
}

/* For slide-out */
.slide-fade-enter-to,
.slide-fade-leave-from {
  transform: rotateX(0deg);
  opacity: 1;
}
</style>
