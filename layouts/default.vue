<template>
  <div>
    <Navbar />
    <slot />
    <Footer />
  </div>
</template>

<script setup>

import Navbar from "~~/components/layout/navbar.vue";
import Footer from "~~/components/layout/Footer.vue";

</script>

<style>

.toolbar {
  background-color: #ffffff;
  color: #1a202c;
}

.sidebar {
  background-color: #ffffff;
  color: #1a202c;
  border-right-color: #ffffff5d;
}


.card {
  background-color: #ffffff;
  border: 1px solid #edf2f7;
}


.light-gray-bg {
  background-color: #f7fafc;
}

.bg-blue-100 {
  background-color: #bfdbfe;
}

.them-switch {
  background-color: #2d374848;
  color: #ffffff;
}
.them-switch:hover {
  background-color: #4a556876;
}

.edf2f7 {
  background-color: #edf2f7;
}


.card-hover:hover {
  background-color: #f7fafc;
  border: 1px solid #f7fafc;
}


.brand{
color: #2563eb;
}

</style>
