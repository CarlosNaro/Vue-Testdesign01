<script setup >
import { computed } from "vue";



const props = defineProps({

  
  avatar: {
    type: String,
    default: "../assets/vue.svg",
  },
  username:{
    type: String,
    default: null,
  }

 
});


const username = computed(() => props.username);
</script>

<template>
  <div class="p-2">
    <img
      :src="props.avatar"
      :alt="username"
    />
  </div>
</template>


