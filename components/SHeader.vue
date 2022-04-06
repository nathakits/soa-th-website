<template>
  <div class="p-10">
    <div
      class="grid gap-8 p-10 rounded-2xl text-white"
      style="background-color: #1d3a54"
    >
      <div class="flex justify-between">
        <div id="header-logo">
          <nuxt-link to="/">
            <img src="~/assets/imgs/soa-thailand.png" />
          </nuxt-link>
        </div>
        <div id="header-nav">
          <nuxt-link
            v-for="(nav, index) in headerLinks"
            :key="index"
            :to="nav.url"
          >
            <p>{{ nav.name }}</p>
          </nuxt-link>
        </div>
      </div>
      <div class="grid grid-cols-9 gap-8">
        <div class="flex flex-col gap-6 justify-between col-span-3">
          <div id="hero-intro">
            <div class="font-bold pb-6">
              <h1>Developing Leaders</h1>
              <h1>Cultivating Ideas</h1>
              <h1>Accelerating Solutions</h1>
            </div>
            <div class="text-xl">
              Our vision is to restore the health of the ocean in our lifetime.
            </div>
          </div>
          <div>
            <s-button>Join Our Community</s-button>
          </div>
        </div>
        <div id="hero-img" class="col-span-6">
          <img class="w-full h-full" src="~/assets/imgs/hero-img.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SButton from './SButton.vue'
export default {
  name: 'SHeader',
  components: { SButton },
  data: () => {
    return {
      headerLinks: [
        {
          name: 'About',
          url: '/about',
        },
      ],
    }
  },
}
</script>
