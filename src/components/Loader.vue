<script setup>

const props = defineProps({
  size: {
    type: String,
    default: '24px',
  },
  color: {
    type: String,
    default: 'black',
  },
})

</script>
<template>
  <span class="loader" :style="
    {
      width: props.size,
      height: props.size,
      borderTopColor: props.color,
    }
  "></span>
</template>
<style scoped>
.loader {
  border-radius: 50%;
  display: inline-block;
  border-top: 4px solid #FFF;
  border-right: 4px solid transparent;
  box-sizing: border-box;
  animation: rotation 1s linear infinite;
}

@keyframes rotation {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
} 
</style>
