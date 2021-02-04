<template>
  <div class="container py-8 xl:px-0">
    <div class="flex flex-col md:flex-row space-y-8 md:space-y-0 md:space-x-8">
      <div
        class="md:space-y-4 hover:shadow-lg transition-shadow duration-500"
        v-for="card in moduleData.cards"
        v-bind:key="card.id"
      >
        <a v-bind:href="card.link.url.href">
          <img v-bind:src="card.image.src" v-bind:alt="card.image.alt" />
        </a>
        <div class="p-4 md:p-8 space-y-4">
          <span class="text-xl font-semibold" v-html="card.subheading"></span>
          <p v-html="card.content"></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  props: ['moduleData'],
  data: function() {
    return {
      // sprocketLogo,
      // vueLogo,
    };
  },
  created: function() {
    // eslint-disable-next-line no-console
    console.log(this.moduleData);
  },
  components: {
    // Card,
    // SpinningLogo
  },
};
</script>
