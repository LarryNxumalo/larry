<template>
  <div ref="scrollSections" class="hello">
    <h1>{{ msg }}</h1>
    <section data-scroll-section>
      <h3 data-scroll data-scroll-speed="1" class="text-3xl font-bold underline">Larry Nxumalo</h3>
      <ul data-scroll data-scroll-speed="2">
        <li>
          <a
            href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel"
            target="_blank"
            rel="noopener"
          >babel</a>
        </li>
        <li>
          <a
            href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint"
            target="_blank"
            rel="noopener"
          >eslint</a>
        </li>
      </ul>
    </section>
    <section data-scroll-section>
      <h3 data-scroll data-scroll-speed="9" data-scroll-direction="horizontal" data-scroll-delay="0.05" style="transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);">Essential Links Left</h3>
      <ul data-scroll data-scroll-speed="2">
        <li>
          <a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a>
        </li>
        <li>
          <a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a>
        </li>
        <li>
          <a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a>
        </li>
        <li>
          <a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a>
        </li>
        <li>
          <a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a>
        </li>
      </ul>
    </section>
    <section data-scroll-section>
      <h3 data-scroll data-scroll-speed="4">Ecosystem</h3>
      <ul data-scroll data-scroll-speed="2">
        <li>
          <a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a>
        </li>
        <li>
          <a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a>
        </li>
        <li>
          <a
            href="https://github.com/vuejs/vue-devtools#vue-devtools"
            target="_blank"
            rel="noopener"
          >vue-devtools</a>
        </li>
        <li>
          <a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a>
        </li>
        <li>
          <a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
import locomotiveScroll from "locomotive-scroll";
export default {
  name: "locoScroll",
  props: {
    msg: String
  },
  data() {
    return {
      scrollIns: null
    };
  },
  mounted() {
    const _self = this;
    this.$nextTick(function() {
      _self.initLocoScroll();
    });
  },
  methods: {
    initLocoScroll() {
      const _self = this;
      this.scroll = new locomotiveScroll({
        el: _self.$refs['scrollSections'],
        smooth: true,
        smoothMobile: true,
        getDirection: true
      });
    }
  }
};
</script>

<style scoped>
section {
  min-height: 600px;
  border-bottom: 1px solid #38495C;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
h3 {
  margin: 40px 0 0;
}
ul {
  display: block;
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
