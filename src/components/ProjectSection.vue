<template>
  <div id="experience">
    <p class="text-3xl text-center md:py-16 py-8 pb-5 font-bold">WORK EXPERIENCE</p>
    <div v-for="(item, index) in projects" :key="index">
      <div
        class="md:flex"
        :class="{ 'flex-row-reverse': index % 2 !== 0 }"
      >
        <div
          class="flex items-center justify-center w-full md:w-1/2"
          :class="{'border-b border-[#286dab] md:border-b-0': index != projects.length-1}"
        >
          <div class="lg:px-16 px-8 py-4">
            <p
              v-html="item.content"
            ></p>
          </div>
        </div>
        <div class="relative overflow-hidden -z-10 md:block hidden" :class="{ 'right-5': index % 2 === 0 }">
          <div class="circle"></div>
          <div class="line"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      projects: [
        {
          content: `<div>
            <p class="text-xl font-bold">
              Member Of Technical Staff - 2 (Blowhorn)
            </p>
            <p class="italic text-teal-500 ">03/2022 - Present,</p>
            <p class="italic text-teal-500">Achievements/Tasks</p>
            <ul style="list-style-type:disc" class="text-lg">
              <li class="py-1">
                Migrated & Developed new design for an existing UI of a product
                to look more user friendly and attractive, which results in
                increased demand by 40% by existing and new clients in the
                market.
              </li>
              <li class="py-1">
                Contributed to project architecture to improve the development
                process and remove the dependency between teams, so everyone can
                work parallel without depending on each other.
              </li>
              <li class="py-1">
                Developed Routes Conﬁguration & ﬂeet overview module with Google
                Map, Marker and Google Autocomplete from scratch which assigns
                routes to the drivers for delivering products and to list the
                available ﬂeet in selected location, hub, vehicle type and
                driver name.
              </li>
              <li class="py-1">
                Developed Wallet module with razorPay and paytm payment gateway
                integration. where user can add money to their wallet using
                multiple payment gateway options, and also can view the credit
                and debit amount along with multiple details.
              </li>
              <li class="py-1 font-semibold">
                Tech Stack:- HTML5, CSS3, Javascript, Vue Js , Nuxt js, Tailwind
                css, PrimeVue.
              </li>
            </ul>
            </div>`,
          id: 1,
        },
        {
          content: `<div>
            <p class="text-xl font-bold">
              Software Engineer (Profinch Solution Pvt Ltd)
            </p>
            <p class="italic text-teal-500 ">02/2019 - 03/2022,</p>
            <p class="italic text-teal-500">Achievements/Tasks</p>
            <ul style="list-style-type:disc" class="text-lg">
              <li class="py-1">
                Developed setups scripts & Reusable Modules, resulting in increased productivity by 50% and reduced development time and cost by 30%.
              </li>
              <li class="py-1">
                Developed new module for introducing new features like Group corporate alert subscription and User alert Subscription for Users in Banking web application. where corporate and retail users can subscribe an multiple alerts like push notiﬁcation,on screen, email & sms alerts for particular account number for any transaction. which enhanced security by 50%.
              </li>
              <li class="py-1">
                Worked on API integration, debugging, bug Fixing for various UI screens. which enhanced the performance of application.
              </li>
              <li class="py-1">
                Meeting with Clients for Project Requirement Analysis and Planning, so we can set a timeline and scope for the project.
              </li>
              <li class="py-1">
                Provide Technical knowledge for the project with 100% client satisfaction.
              </li>
              <li class="py-1 font-semibold">
                Tech Stack:- Tech Stack:- HTML5, CSS3, Javascript, ReactJs, KnockoutJs, Material UI 
              </li>
            </ul>
            </div>`,
          id: 2,
        },
      ],
    };
  },
};
</script>
<style scoped>
.circle {
  background-color: rgb(255, 255, 255);
  border: 3px solid gray;
  border-radius: 100%;
  width: 20px; /* +6 for border */
  height: 20px;
}
.line {
  top: 20px;
  left: 9px;
  height: 100%;
  position: absolute;
  border-left: 3px solid gray;
}
</style>
