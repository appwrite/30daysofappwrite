<template>
  <div class="flex flex-col min-h-screen">
    <Header />
    <HelloWorld />
    <Timeline />
    <Tweets />
    <Swags />
    <Resources />
    <Footer />
  </div>
</template>

<script setup>
import Header from "./components/Header.vue";
import HelloWorld from "./components/HelloWorld.vue";
import Timeline from "./components/Timeline.vue";
import Tweets from "./components/Tweets.vue";
import Resources from "./components/Resources.vue";
import Swags from "./components/Swags.vue";
import Footer from "./components/Footer.vue";
</script>
