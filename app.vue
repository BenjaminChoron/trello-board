<script setup>
const showTips = ref(false);
</script>

<template>
  <div class="p-10 h-[100dvh] bg-teal-600 overflow-auto">
    <h1 class="text-4xl text-white flex items-center mb-10">Trello Board</h1>

    <button @click="showTips = !showTips"
      class="absolute top-10 right-10 text-white border border-white rounded-full w-8 h-8 flex items-center justify-center bg-teal-800 hover:bg-teal-700 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-opacity-50">
      ?
    </button>

    <div v-if="showTips" @click="showTips = !showTips"
      class="z-10 absolute top-0 left-0 w-full h-[100dvh] bg-teal-800 opacity-50" />
    <dialog open v-if="showTips" class="z-20 rounded shadow p-5">
      <h2 class="font-bold text-center">Tips</h2>

      <button @click="showTips = !showTips"
        class="absolute top-2 right-2 text-white border border-white rounded-full w-6 h-6 flex items-center justify-center bg-teal-800 hover:bg-teal-700 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-opacity-50">
        X
      </button>

      <ul>
        <li class="m-5 text-xs italic">
          To drag a column or a task, hold the
          <code class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded">⋮⋮</code>
          symbol
        </li>

        <li class="m-5 text-xs italic">
          You can clone a task holding
          <code class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded">alt</code>
          or
          <code class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded">opt</code>
          key when dragging
        </li>

        <li class="m-5 text-xs italic">
          To edit a column title, just click on it, write your text and tap <code
            class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded">↵</code>
        </li>

        <li class="m-5 text-xs italic">
          To delete a column, click on the title, delete all the text of the input and tap <code
            class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded">⌫</code>
        </li>

        <li class="m-5 text-xs italic">
          To delete a task, click on it and tap <code
            class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded">⌫</code>
        </li>
      </ul>
    </dialog>

    <TrelloBoard />
  </div>
</template>
