<template>
  <div class="container" v-if="seoData && seoData.texts">
    <div class="row g-5">
      <div class="col-lg-8 fadeInUp" style="min-height: 400px">
        <div v-if="seoData && seoData.texts">
          <div v-for="(text, index) in seoData.texts" :key="index">
            <div class="mb-3 mt-5 h2" v-html="text.title"></div>
            <p class="mb-4" v-html="text.text"></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "seoText",
  props: {
    seoData: Object,
  },
};
</script>
