<script setup lang="ts">
function onClick(x: number, y: number) {
  console.log(`x: ${x} y: ${y}`)
}
</script>

<template>
  <div>
    Minesweeper

    <div v-for="y in 10" :key="y">
      <button
        v-for="x in 10"
        :key="x"
        w-10 h-10 border hover:bg-gray
        @click="onClick(x, y)"
      >
        {{ (y - 1) * 10 + x }}
      </button>
    </div>
  </div>
</template>
