<template>
  <div>
    <base-Navbar />
    <module-landingpage-LandingPage />
    <base-Footer />
  </div>
</template>

<script setup>
import { useStore } from "@/store/index.js";
import { onMounted } from "vue";

const test = useStore();

onMounted(() => {
  console.log(test.selectedMenu);
});
</script>
