<template>
  <div class="flex">
    <button
      @click="updateSortedDir('asc')"
      class="bg-gray-800 hover:bg-gray-400 text-white py-2 px-2 rounded-md"
    >
      Sort Ascending
    </button>
    <button
      @click="updateSortedDir('desc')"
      class="bg-gray-800 hover:bg-gray-400 text-white py-2 px-2 ml-4 rounded-md"
    >
      Sort Descending
    </button>
  </div>
</template>

<script setup>
const emits = defineEmits(["update-sorting-direction"]);
const props = defineProps({
  currentSortDir: {
    type: String,
    required: true,
  },
});
const updateSortedDir = (newSortDir) => {
  emits("update-sorting-direction", newSortDir);
};
</script>

<style lang="scss" scoped></style>
