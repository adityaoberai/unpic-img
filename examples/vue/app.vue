<script setup lang="ts">
import { Image } from "@unpic/vue";
import { Image as BaseImage } from "@unpic/vue/base";
import { transform } from "unpic/providers/imgix";
</script>
<template>
  <BaseImage src="https://images.unsplash.com/photo-1617718295766-0f839c2853e7" layout="fullWidth" alt="fullWidth"
    :aspectRatio="16 / 9" priority :transformer="transform" :operations="{ flip: 'v' }" />
  <Image src="https://cdn.shopify.com/static/sample-images/garnished.jpeg" layout="constrained" width="800" height="600"
    alt="constrained" />
  <Image src="https://bunnyoptimizerdemo.b-cdn.net/bunny7.jpg" width=800 height=600 layout="fixed" alt="fixed"
    :operations="{
      bunny: {
        flop: true,
      },
    }" />
  <div style="height: 10000px"></div>
  <Image src="https://cdn.shopify.com/static/sample-images/bath.jpeg" layout="constrained" width=600 height=800
    alt="offscreen" />
</template>
<style>
body {
  margin: 0;
}
</style>
