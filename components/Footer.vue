<template>
  <div
    class="max-h-full max-w-full bg-slate-900 text-slate-300 font-serif md:px-12 p-12"
  >
    <div class="max-w-4xl mx-auto flex flex-col items-center justify-center">
      <h1 class="text-2xl sm:text-4xl leading-tight m-3">
        {{ "Coffee with me." }}
      </h1>
      <p class="text-xs md:text-xl">
        {{
          "I am always excited to work on some awesome projects, message me and let's discuss over coffee."
        }}
      </p>
      <div class="max-w-full md:w-5/6">
        <MessageForm />
      </div>
    </div>
    <div class="flex flex-col justify-center items-center md:flex-row md:items-center md:justify-between mx-auto">
      <div class="flex flex-col items-center justify-center md:items-start md:w-4/12 my-4">
        <p class="font-thin">
          {{ "No copyright "
          }}<span class="inline-block align-middle"><IconCopyright /></span
          >{{ " issues." }}
        </p>
        <p class="font-thin">
          {{ "Feel free to copy. If you need any help, ping me !" }}
        </p>
      </div>
      <div class="flex flex-col items-center my-4">
        <h1 class="m-4 text-6xl formathead">{{ "Vipul Jain" }}</h1>
        <p>
          {{ "Made with " }}<span class="text-red-600">❤</span>{{ " in India" }}
        </p>
      </div>
      <sociallinks class="md:w-4/12 my-4" />
    </div>
  </div>
  <div class="w-full flex justify-center"><img src="/footer.webp" /></div>
</template>
<script setup></script>
<style>
.formathead {
  font-family: "Sacramento", cursive;
  text-transform: none;
  font-weight: 400;
  color: #41b0bf !important;
  font-size: 3em !important;
}
</style>
