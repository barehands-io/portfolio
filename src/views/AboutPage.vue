<template>
  <div class="flex justify-center h-screen">
    <main v-if="false" class="flex flex-col lg:flex-row items-center justify-center">
      <div class="lg:w-[600px] regular-text pt-10">
        <p>
          Hello! My name is Sam and I enjoy creating useful things for the
          internet. My interest in web development started back in 2015 when I
          decided to make a website using Adobe Muse — i felt very limited and
          constrained and ultimately that sparked my interest to learn more
          about Html, Css and Javascript.
        </p>
        <br />

        <p>
          Fast-forward to today, and I’ve had the privilege of working at a web
          development agencies , a start-up,and a huge music Streaming platform.
          <br />
          My main focus these days is building accessible, inclusive products
          and digital experiences at as a free lancer.
        </p>
        <br />
        <ul class="flex gap-x-10">
          <li v-for="(item, index) in contacts" :key="index">
            <a :href="item.link"
            ><i :class="item.image"></i
            ><span class="underline pl-2"> {{ item.social }}</span></a
            >
          </li>
        </ul>
        <br />
        <div>
          <ButtonComponent
            @click="downloadResume"
            title="Download Resume"
            icon="fal fa-cloud-download"
          />
        </div>
      </div>
      <ProfileImage />
    </main>


    <div class=" mx-auto  p-6 rounded-lg  text-justify regular-text">
      <h1 class="text-2xl font-bold mb-4">Hello! My name is <span class="text-blue-500">Harry</span>.</h1>

      <p class="mb-4">
        I have a passion for crafting innovative digital solutions that don't just look great but also drive business
        results. If you're a business owner looking to enhance your online presence, <span class="font-semibold">I'm here to help</span>.
      </p>

      <p class="mb-4">
        In today's digital age, a functional and intuitive online interface isn't just an asset—it's essential. I
        specialize in creating websites and applications that offer engaging user experiences, ensuring that your
        customers stay longer and engage more with your brand.
      </p>

      <p class="mb-4">
        But beyond the technical aspects, I focus on understanding the unique needs and goals of each business. Whether
        you're aiming to increase online sales, boost customer engagement, or simply provide valuable information to
        your audience, I can create a digital solution that aligns with your objectives.
      </p>

      <p class="mb-4">
        Every touchpoint on a website or application is an opportunity—a chance to impress a customer, to simplify their
        journey, or to close a sale. I understand this deeply, and it drives my approach. The digital solutions I craft
        are not only about aesthetic appeal; they're strategically designed to grow and support your business.
      </p>

      <p class="mb-4">
        In the ever-evolving digital landscape, staying ahead of the curve can be a challenge for any business owner.
        Allow me to take that weight off your shoulders. Together, we can shape your online presence, making it both
        memorable for your audience and profitable for your business.
      </p>

      <p>
        If you're seeking a digital partner who understands the intersection of design, functionality, and business
        impact, I'd be thrilled to discuss how we can collaborate and elevate your online presence.
      </p>
    </div>

  </div>
</template>
<script setup lang="ts">
import ProfileImage from "../components/ProfileImage.vue";
import ButtonComponent from "@/views/ButtonComponent.vue";

const contacts = [
  {
    social: "LinkedIn",
    link: "https://www.linkedin.com/in/chibueze-samuel-nmeje-088508a2/",
    image: "fab fa-linkedin"
  },

  /*  {
    social: "Twitter",
    link: "",
    image: "fab fa-twitter",
  },*/
  {
    social: "Samuelnmeje@gmail.com",
    link: "mailto:samuelnmeje@gmail.com?Subject=Enquiry",
    image: "fal fa-envelope"
  }
];

const introduction = `

Hello! My name is Harry. I have a passion for crafting innovative digital solutions that don't just look great but also drive business results. If you're a business owner looking to enhance your online presence, I'm here to help.

In today's digital age, a functional and intuitive online interface isn't just an asset—it's essential. I specialize in creating websites and applications that offer engaging user experiences, ensuring that your customers stay longer and engage more with your brand. With tools like React and Vue at my fingertips, I design scalable, responsive, and user-friendly platforms tailored to your business needs.

But beyond the technical aspects, I focus on understanding the unique needs and goals of each business. Whether you're aiming to increase online sales, boost customer engagement, or simply provide valuable information to your audience, I can create a digital solution that aligns with your objectives.

Every touchpoint on a website or application is an opportunity—a chance to impress a customer, to simplify their journey, or to close a sale. I understand this deeply, and it drives my approach. The digital solutions I craft are not only about aesthetic appeal; they're strategically designed to grow and support your business.

In the ever-evolving digital landscape, staying ahead of the curve can be a challenge for any business owner. Allow me to take that weight off your shoulders. Together, we can shape your online presence, making it both memorable for your audience and profitable for your business.

If you're seeking a digital partner who understands the intersection of design, functionality, and business impact, I'd be thrilled to discuss how we can collaborate and elevate your online presence.


`;

function downloadResume() {
  const link = document.createElement("a");
  link.href = "src/downloads/front-end-developer-vue.pdf";
  link.download = "front-end-developer-vue.pdf";

  link.click();
}
</script>
