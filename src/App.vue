<template>
  <div
    class="w-screen h-screen flex items-center justify-center bg-gray-50 dark:bg-gray-900 px-5"
  >
    <div
      class="bg-white dark:bg-gray-800 shadow-xl w-full sm:w-10/12 md:w-8/12 lg:w-6/12 p-6"
    >
      <h4
        class="font-semibold text-md mb-3 border-b border-gray-200 dark:text-gray200"
      >
        Login
      </h4>
      <div class="space-y-3">
        <input type="email" class="inputStyle" placeholder="E-mail" />
        <input type="password" class="inputStyle" placeholder="Senha" />

        <div class="text-right">
          <button
            class="rounded text-sm px-3 py-2 bg-green-400 hover:bg-green-500 text-green-900"
          >
            LOGIN
          </button>
        </div>
      </div>
    </div>
  </div>
  <DarkModeSwitch />
</template>

<style>
.inputStyle {
  @apply px-3 py-2 placeholder-gray-200 border border-gray-300 dark:border-gray-600 dark:text-gray-200 w-full dark:bg-gray-700;
}
</style>

<script>
import DarkModeSwitch from "./components/DarkModeSwitch";
export default {
  name: "App",
  components: {
    DarkModeSwitch,
  },
};
</script>
