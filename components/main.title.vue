<template>
  <div>
    <h1 class="text-xl md:text-4xl text-center overflow-hidden">
      Every <br />
      <span class="font-bold text-[#f2740d]">
        <TypeEffect :externalArray="roles" />
      </span>
      requires <span class="text-blue-600">tech solutions</span>
    </h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      roles: [
        "Pharmacy",
        "Trade",
        "Finance",
        "Healthcare",
        "Retail",
        "Manufacturing",
        "Entertainment",
        "Education",
        "Automotive",
        "Hospitality",
        "Energy",
        "Agriculture",
        "Individual",
        "Telecommunications",
        "Real Estate",
        "Construction",
        "Transportation",
        "Aerospace",
        "Media",
        "Non-profit",
        "Government",
        "Consulting",
        "Legal",
        "Fashion",
        "Food and Beverage",
        "Travel",
        "Environmental",
        "Fitness",
        "Art and Design",
        "Insurance",
        "Biotechnology",
        "Research",
        "Pharmaceuticals",
        "Renewable Energy",
      ],
      currentRoleIndex: 0,
      containerWidth: "411px",
      containerHeight: "72px",
    };
  },
  methods: {
    startAnimation() {
      setInterval(() => {
        this.currentRoleIndex = (this.currentRoleIndex + 1) % this.roles.length;
      }, 2000);
    },
  },
  mounted() {
    this.startAnimation();
  },
};
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5ms;
}
.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
}
</style>
