<template>
  <div class="flex flex-col items-center px-8">
    <Logo />
    <h1 class="mt-4 text-4xl font-bold text-center">30 Days of Appwrite</h1>
    <p class="max-w-3xl mt-4 text-center text-gray-500 text-md md:text-lg">
      Work towards becoming a better developer by going through the awesome
      resources that we've compiled for you. This covers all the basic and
      advanced features of
      <a href="https://appwrite.io" target="_blank" rel="noopener">Appwrite</a>
      that you need, to build your next app. Take advantage of the amazing
      content out there for free, set your right mindset and get going!
    </p>
    <div
      class="flex flex-col items-center justify-center mt-8 space-y-4 md:space-x-6 md:space-y-0 md:flex-row"
    >
      <a
        href="https://dev.to/appwrite"
        target="_blank"
        rel="noopener"
        class="bg-pink-500 hover:bg-pink-600 button"
        >Join 30 Days of Appwrite</a
      >
      <a
        href="https://twitter.com/search?q=%2330DaysofAppwrite"
        target="_blank"
        rel="noopener"
        class="bg-blue-400 hover:bg-blue-500 button"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="24"
          width="24"
          viewBox="0 0 512 512"
          class="mr-2"
        >
          <path
            fill="currentColor"
            d="M512 97.248c-19.04 8.352-39.328 13.888-60.48 16.576 21.76-12.992 38.368-33.408 46.176-58.016-20.288 12.096-42.688 20.64-66.56 25.408C411.872 60.704 384.416 48 354.464 48c-58.112 0-104.896 47.168-104.896 104.992 0 8.32.704 16.32 2.432 23.936-87.264-4.256-164.48-46.08-216.352-109.792-9.056 15.712-14.368 33.696-14.368 53.056 0 36.352 18.72 68.576 46.624 87.232-16.864-.32-33.408-5.216-47.424-12.928v1.152c0 51.008 36.384 93.376 84.096 103.136-8.544 2.336-17.856 3.456-27.52 3.456-6.72 0-13.504-.384-19.872-1.792 13.6 41.568 52.192 72.128 98.08 73.12-35.712 27.936-81.056 44.768-130.144 44.768-8.608 0-16.864-.384-25.12-1.44C46.496 446.88 101.6 464 161.024 464c193.152 0 298.752-160 298.752-298.688 0-4.64-.16-9.12-.384-13.568 20.832-14.784 38.336-33.248 52.608-54.496z"
          />
        </svg>
        #30DaysofAppwrite</a
      >
    </div>
  </div>
</template>

<style scoped>
.button {
  @apply inline-flex;
  @apply items-center;
  @apply justify-center;
  @apply text-white;
  @apply font-bold;
  @apply px-6;
  @apply py-3;
  @apply rounded-full;
  @apply hover:text-white;
}
a {
  @apply text-pink-600;
}
a:hover {
  @apply text-pink-800;
}
</style>

<script setup>
import Logo from "../components/Logo.vue";
</script>
