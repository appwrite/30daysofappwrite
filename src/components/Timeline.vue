<template>
  <h1 class="mx-6 mt-24 mb-8 text-4xl font-bold">⏰ Timeline</h1>
  <div class="relative flex flex-col flex-1 mx-6 my-4">
    <div
      class="absolute top-0 h-full border-r-4 border-gray-200"
      style="z-index: -1; left: 26px"
    ></div>
    <ul class="flex flex-col justify-end space-y-8 md:space-y-10">
      <li
        v-for="(event, index) in timeline.slice(0, itemsCount)"
        :key="`event-${index}`"
        class="event-item"
      >
        <div class="event-heading">
          <div
            class="event-indicator"
            :class="
              new Date(event.date) > new Date() ? 'bg-gray-400' : 'bg-green-500'
            "
          >
            {{ index + 1 }}
          </div>
          <component
            :is="event.link ? 'a' : 'div'"
            :href="event.link"
            target="_blank"
            rel="noopener"
            class="event-headline"
          >
            <span class="event-title">{{ event.title }}</span>
          </component>
        </div>
        <div v-if="event.description" class="event-description">
          {{ event.description }}
        </div>
        <div class="flex ml-20">
          <a
            v-if="event.link"
            :href="event.link"
            target="_blank"
            rel="noopener"
            class="button"
          >
            Read article
          </a>
        </div>
        <div class="event-date">
          {{
            new Intl.DateTimeFormat("en-US", {
              month: "short",
              day: "numeric",
            }).format(new Date(event.date))
          }}
        </div>
      </li>
    </ul>
  </div>
  <div v-if="itemsCount < timeline.length" class="more-container">
    <button class="more-event" @click="itemsCount += 5">Show more</button>
  </div>
</template>

<style scoped>
.event-item {
  @apply flex;
  @apply flex-col;
}
.event-heading {
  @apply flex;
}
.event-indicator {
  @apply flex;
  @apply items-center;
  @apply justify-center;
  @apply flex-shrink-0;
  @apply w-14;
  @apply h-14;
  @apply border-8;
  @apply text-white;
  @apply border-white;
  @apply rounded-full;
}
.event-headline {
  @apply ml-6;
  @apply mt-3;
}
.event-title {
  @apply font-bold;
  @apply text-2xl;
}
.event-description {
  @apply mt-2;
  @apply ml-20;
  @apply text-gray-600;
  @apply max-w-2xl;
}
.event-date {
  @apply mt-2;
  @apply ml-20;
  @apply text-sm;
  @apply text-gray-400;
}
a {
  @apply text-pink-400;
  @apply hover:text-pink-500;
}
.more-container {
  @apply flex;
  @apply items-center;
  @apply justify-center;
  @apply h-0;
  @apply border-b-2;
  @apply border-dashed;
  @apply border-gray-300;
  @apply mx-6;
}
.more-event {
  @apply flex;
  @apply items-center;
  @apply justify-center;
  @apply absolute;
  @apply px-6;
  @apply py-3;
  @apply font-bold;
  @apply bg-pink-400;
  @apply text-white;
  @apply rounded-full;
  @apply focus:outline-none;
  @apply hover:bg-pink-500;
}
.button {
  @apply flex;
  @apply border-2;
  @apply rounded-lg;
  @apply py-1;
  @apply px-3;
  @apply font-bold;
  @apply my-4;
  @apply border-pink-400;
  @apply hover:border-pink-500;
}
</style>

<script>
import data from "../assets/data/timeline";

export default {
  setup() {
    return {
      timeline: data,
    };
  },
  data() {
    return {
      itemsCount: 5,
    };
  },
};
</script>
