<template>
  <div>
    <!-- دکمه‌ی تغییر وضعیت -->
    <button @click="toggleDarkMode">
      {{ isDark ? "حالت روشن" : "حالت تاریک" }}
    </button>

    <!-- یک دکمه‌ی نمونه که از dark: استفاده کرده -->
    <button class="bg-white dark:bg-gray-800 text-black dark:text-white">
      دکمه‌ی نمونه
    </button>
  </div>
</template>

<script setup>
const isDark = ref(false); // متغیر وضعیت

// تابع تغییر وضعیت
const toggleDarkMode = () => {
  isDark.value = !isDark.value;
  if (isDark.value) {
    document.documentElement.classList.add("dark");
  } else {
    document.documentElement.classList.remove("dark");
  }
};
</script>
