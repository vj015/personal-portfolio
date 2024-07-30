<template>
  <div
    class="max-h-full max-w-full bg-slate-300 text-slate-900 font-serif md:px-12 py-12"
  >
    <div class="max-w-4xl mx-auto flex flex-col items-center">
      <h1 class="text-2xl sm:text-4xl leading-tight m-3">
        {{ "Professional Experience" }}
      </h1>
      <div class="max-w-full my-5">
        <CrouselSlide :slides="slides" />
      </div>
      <div class="flex flex-row flex-wrap m-2 justify-center">
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Vue
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Nuxt
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          React
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Spring
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Reactive Programming
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Temporal
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Tailwind
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Sendgrid
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Java
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Javascript
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Feature Flags
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          Jest
        </button>
        <button
          class="bg-transparent hover:bg-slate-900 text-slate-900 font-semibold hover:text-slate-300 py-2 px-4 border border-slate-900 hover:border-transparent rounded text-xl m-1"
        >
          SASS
        </button>
      </div>
    </div>
  </div>
</template>
<script setup>
const slides = ref([
  {
    title: "SDE Intern: Payments Team @ Maersk",
    content:
      "During probation, Vipul worked on the Surcharge Feature MVP 1.0, which is now implemented for US customers. This feature helps Maersk recover costs that are deducted from our bottom line, approximately $2.9 million per month, incurred through credit card payments via Stripe.",
  },
  {
    title: "Associate SDE: Payments Team @ Maersk",
    content:
      "Worked on migrating the payment capabilities of MAERSK from the existing Biller Direct system to the new My Finance platform as part of the Payments Team. Focused primarily on integrating UI of ICBC UnionPay for Chinese customers and Doku for Indonesian customers.This system handles approximately 20k transactions per month, accounting for millions of dollars in monthly revenue for Maersk",
  },
  {
    title: "Associate SDE: Payments Team @ Maersk",
    content:
      "Led the integration of HSBC Razorpay Payments from Proof of Concept (POC) to MVP 1.0 for Indian customers. This initiative enables digital payments through UPI and internet banking, enhancing the payment experience for customers in India.",
  },
  {
    title: "SDE: Payments Team @ Maersk",
    content:
      "In addition to payment integrations with various vendors, Vipul also contributed to other projects including Vue migration from V2.6 to V3.2, Sitecore integration, Grafana integration for observability, upgrading email templates via SendGrid, and performance optimizations and enhancements focused on Web Vitals.",
  },
  {
    title: "SDE: Payments Team @ Maersk",
    content:
      "Increased unit test coverage, improved performance and optimization for Payments UI application in Maersk which is handling around 35K monthly transactions in different currencies world wide. Received the 'Star of the Quarter' award for outstanding performance.",
  },
]);
</script>
<style></style>
