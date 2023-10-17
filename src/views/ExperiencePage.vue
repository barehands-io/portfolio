<template>
  <div>
    <div class="regular-text lg:px-10 py-20">
      <div></div>
      <div class="col-span-2 lg:p-2">
        <div class="lg:flex">
          <div class="hidden lg:inline space-y-2"></div>
          <div class="space-y-4">
            <div class="">
              <div class="">
                <div
                  class="tab"
                  v-for="(item, index) in experiences"
                  :key="index"
                >
                  <h1 class="text-xl font-medium">
                    {{ item.role }}
                  </h1>
                  <h1 class="text-green-600 dark:text-green-400 font-medium">
                    {{ item.company }}
                  </h1>
                  <div class="pt-2">
                    <ul class="space-y-2">
                      <li
                        v-for="(item, index) in item.description"
                        :key="index"
                        class=""
                      >
                        <div class="flex gap-x-2">
                          <i class="fal fa-caret-right"></i>
                          <p>{{ item }}</p>
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const experiences = ref([
  {
    company: " Best ChoiceMechanical",
    role: "Software Engineer",
    location: " United State of America",
    description: [
      "Developed a web portal application utilizing MERN Stack in 2 months, resulting in 40% increased user engagement.\n",
      "TDD/BDD methodologies. • Integrated AWS for cloud computing, ensuring scalable and robust application deployment.",
      "Delivered several WordPress websites and web application for small to medium-sized businesses.",
      "Developed websites from front to backend using Vue js, Node js, and Mongodb.",
      "Optimized web portal application architecture, reducing page loading time by 50% in 2 months, utilizing MERN Stack and React.",
    ],
  },
  {
    company: "EdeenBull",
    role: "Lead Software Engineer",
    location: "",
    description: [
      "Developed RESTful APIs using Node.js, Express, and MongoDB. • Established automated testing workflows with Jest, Enzyme, and Cypress.",
      "Engaged in pair programming, Agile stand-ups, and implemented CI/CD processes using Jenkins.",
      " Utilized Docker and Kubernetes for efficient containerization and application deployment.",
      "Developed a web portal application utilizing MERN Stack with improved performance metrics, increasing efficiency by 25% in 3 months.",
      "Leveraged AWS for cloud computing, ensuring seamless application deployment.\n",
    ],
  },
  {
    company: "Katalyst Technologies",
    role: "Lead Front End Developer",
    location: "",
    description: [
      "Designed mobile applications with React Native for Android and iOS platforms.",
      "Manage website development projects from initial design through completion, optimizing all cross-browser and multi-platform compatibility.",
      "Work closely with programmers and clients to meet project requirements, goals, and desired functionality.",
      "Delivered several WordPress websites and web application for small to medium-sized businesses.",
      "Developed websites from front to backend using Vue js, Node js, and Mongodb.",
      "Conduct training for clients on handling website content management systems.",
      "Enhanced application deployment using Docker and Kubernetes.",
    ],
  },

  {
    company: "Wildstream Music",
    role: "Product Designer",
    description: [
      "Performed ideation, sketching and wireframing.",
      "Assessed UX and UI design for technical feasibility and usability",
      "Collaborated with product team members to implement new features development",
    ],
  },
  {
    company: "Disenvi",
    role: "Lead designer",
    description: [
      "Implemented websites, mobile application, and landing pages from concept to development",
      "Standardized all output with a new, responsive, mobile-first approach and strategy",
      "Assessed UX and UI design for technical feasibility and usability",
      "collaborated with product team members to implement new featues development",
    ],
  },
]);
</script>

<style lang="scss"></style>
