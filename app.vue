<template>
  <div class="p-10 h-[100dvh] bg-teal-600 overflow-auto">
    <h1 class="text-4xl text-white flex items-center mb-10">Trello Board</h1>

    <p class="m-5 text-white text-xs italic">
      To drag a column or a task, hold the
      <code
        class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded"
        >⋮⋮</code
      >
      symbol
    </p>
    <p class="m-5 text-white text-xs italic">
      You can clone a task holding
      <code
        class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded"
        >alt</code
      >
      or
      <code
        class="p-1 text-black not-italic bg-gray-50 border border-gray-500 rounded"
        >opt</code
      >
      key when dragging
    </p>

    <TrelloBoard />
  </div>
</template>
