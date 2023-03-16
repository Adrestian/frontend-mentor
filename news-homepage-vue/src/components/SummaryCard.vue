<template>
  <div
    class="max-w-[750px] rounded-3xl overflow-hidden bg-white shadow-xl text-neutral-900 flex flex-col sm:flex-row"
  >
    <!-- Result pane -->
    <div
      class="shadow-neutral-200 shadow-2xl w-[375px] bg-gradient-to-b from-indigo-500 to-blue-500 rounded-3xl py-8"
    >
      <h2 class="text-4xl capitalize text-neutral-100 text-center">Your Result</h2>
      <!-- rounded ball -->
      <div
        class="grid place-items-center mt-6 bg-gradient-to-b from-indigo-600 to-transparent w-[200px] h-[200px] rounded-full mx-auto"
      >
        <div class="">
          <div class="text-white text-7xl mx-auto text-center">60</div>
          <div class="text-neutral-300 mt-4 text-center">of&nbsp;&nbsp;100&nbsp;&nbsp;&nbsp;</div>
        </div>
      </div>
      <div class="text-neutral-50 text-4xl text-center mt-6">Great</div>
      <p class="text-neutral-200 leading-5 text-center mt-4 w-[60%] mx-auto">
        You scored higher than 65% of the people who have taken these tests
      </p>
    </div>
    <!-- summary pane-->
    <div class="text-xl w-[375px] px-8">
      <h1 class="text-xl text-neutral-600 py-4 font-semibold">Summary</h1>
      <div class="space-y-4 tracking-tighter">
        <section
          class="w-full px-8 py-3 rounded-lg flex items-center justify-between bg-red-100 text-red-600"
        >
          <div>Reaction</div>
          <div class="text-neutral-500">
            <span class="text-slate-700 font-bold">80</span>&nbsp;&nbsp;/&nbsp;&nbsp;100
          </div>
        </section>
        <section
          class="px-8 py-3 rounded-lg flex items-center justify-between bg-yellow-100 text-yellow-600"
        >
          <div>Memory</div>
          <div class="text-neutral-500">
            <span class="text-slate-700 font-bold">92</span>&nbsp;&nbsp;/&nbsp;&nbsp;100
          </div>
        </section>
        <section
          class="px-8 py-3 rounded-lg flex items-center justify-between bg-teal-100 text-teal-600"
        >
          <div>Verbal</div>
          <div class="text-neutral-500">
            <span class="text-slate-700 font-bold">61</span>&nbsp;&nbsp;/&nbsp;&nbsp;100
          </div>
        </section>
        <section
          class="px-8 py-3 rounded-lg flex items-center justify-between bg-blue-100 text-blue-500"
        >
          <div>Visual</div>
          <div class="text-neutral-500">
            <span class="text-slate-700 font-bold">81</span>&nbsp;&nbsp;/&nbsp;&nbsp;100
          </div>
        </section>
      </div>
      <button
        class="bg-slate-700 text-slate-50 py-4 w-full rounded-full my-8 hover:bg-slate-800 duration-300 cursor-pointer"
      >
        Continue
      </button>
    </div>
  </div>
</template>
<script setup></script>
