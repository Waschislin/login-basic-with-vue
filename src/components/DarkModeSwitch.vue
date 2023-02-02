<template>
  <div
    class="absolute top-0 right-0 p-4 cursor-pointer dark:text-gray-300"
    @click="toggle"
  >
    <p>{{ name }}</p>
  </div>
</template>

<script>
export default {
  name: "DarkModeSwitch",
  data() {
    return {
      isDark: false,
    };
  },
  computed: {
    name() {
      return this.isDark ? "Light" : "Dark";
    },
  },
  watch: {
    isDark(vl) {
      const htmlEl = document.getElementsByTagName("html")[0];
      if (vl) {
        htmlEl.classList.add("dark");
      } else {
        htmlEl.classList.remove("dark");
      }
    },
  },
  methods: {
    toggle() {
      this.isDark = !this.isDark;
    },
  },
};
</script>
