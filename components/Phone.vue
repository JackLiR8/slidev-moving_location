<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  img: {
    type: String,
    required: true,
  },
})

</script>

<template>
  <div class="phone">
    <img class="phone-img" :src="props.img" />
  </div>
</template>

<style scoped>
.phone {
  height: 50vh;
  width: 22.5vh;
  overflow: hidden;
  border-radius: 1rem;
  box-shadow: 0 0 0.5rem 0.5rem rgba(0, 0, 0, 0.1);
}
.phone-img {
  height: 100%;
  width: 100%;
}
</style>
