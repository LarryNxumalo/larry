<template>
  <div ref="scrollSections" class="p-0 h-full w-full m-0 bg-black relative overflow-hidden overflow-x-hidden">
      <!-- <div class="w-full h-full bg-green-700 flex fixed" >
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700" ></div>
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700"></div>
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700">
          <h1 class="text-9xl stroke-1 stroke-rose-700 text-white">+27 81 437 0235</h1>
        </div>
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700"></div>
      </div>  -->
      <div class="w-full h-full bg-black flex fixed">
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700 flex flex-wrap mt-80 relative">
          <img alt="za-flag" class="w-32 h-32 mx-auto" src="../assets/whiteza.png">
          <p class="text-9xl font-extralight text-left mb-68">sbwl@larrynxumalo.com</p>
        </div>
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700 hover:bg-red-600 hover:text-white inline-block ease-in-out duration-500">
          <p class="text-9xl text-thin">Blasé!</p>
          <p class="mb-32 text-9xl text-thin">Blasé!</p>
          <h2 class="text-white tracking-widest text-transform-upper font-black mb-16">1944-2015</h2>
          <p class="text-white tracking-widest uppercase flex flex-initial">
            School history textbooks are seen to embody ideological messages about whose history is important, 
            as they aim both to develop an 'ideal' citizen and teach the subject of history. Since the 1940s, 
            when the first study was done, there have been studies of South African history textbooks that have analysed different aspects of textbooks. 
            These studies often happen at a time of political change (for example, after South Africa became a republic in 1961 or post-apartheid) 
            which often coincides with a time of curriculum change. This article provides an overview of all the studies of South African history textbooks since the 1940s. 
          </p>
        </div>
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700">
          <h1 class="text-9xl text-red-700">+27 81 437 0235</h1>
        </div>
        <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700">
          <p class="verticalal font-extrabold my-auto mx-auto">#VERTICAL</p>
        </div>
      </div>
    <section class="bg-black w-full h-screen p-0 m-0 " data-scroll-section>

       <div class="w-full h-full bg-black flex fixed">
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700 hover:bg-white hover:text-white inline-block ease-in-out duration-300" data-scroll data-scroll-speed="12" data-scroll-direction="vertical" data-scroll-delay="0.05"></div>
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700 hover:bg-red-600 hover:text-white inline-block ease-in-out duration-300" data-scroll data-scroll-speed="12" data-scroll-direction="horizontal" data-scroll-delay="0.05"></div>
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700" data-scroll data-scroll-speed="-12" data-scroll-direction="vertical" data-scroll-delay="0.05">
             <!-- <h1 class="text-9xl text-black">+27 81</h1> -->
             <h1 class="text-9xl text-gray-900">+27 81</h1>
             <h1 class="text-9xl text-gray-900">+27 81</h1>
             <h1 class="text-9xl text-gray-900">+27 81</h1>
             <h1 class="text-9xl text-gray-700">+27 81</h1>
             <h1 class="text-9xl text-gray-700">+27 81</h1>
             <h1 class="text-9xl text-gray-700">+27 81</h1>
             <h1 class="text-9xl text-white">+27 81</h1>
             <h1 class="text-9xl text-white">+27 81</h1>
            </div>
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700" data-scroll data-scroll-speed="-12" data-scroll-direction="horizontal" data-scroll-delay="0.05"></div>
        </div>
    </section>
    <section class="bg-black w-full h-screen p-0 m-0 relative" data-scroll-section>
        <div class="w-full p-4 bg-white hover:bg-red-600 hover:text-white inline-block ease-in-out duration-300" data-scroll data-scroll-speed="12" data-scroll-direction="horizontal" data-scroll-delay="0.05" >
            <h1 class="relative text-9xl text-black font-black text-center hover:text-white ">LARRY</h1>
        </div>
        <div class="w-full p-4 bg-white" data-scroll data-scroll-speed="12" data-scroll-direction="horizontal" data-scroll-delay="0.9" >
            <h1 class="text-9xl text-red-700 font-black text-center">TINYIKO</h1>
        </div>
        <div class="w-full p-4 border border-1 border-white" data-scroll data-scroll-speed="-6" data-scroll-direction="horizontal" data-scroll-delay="1" >
            <h1 class="text-9xl text-white font-black text-center">NXUMALO &copy;</h1>
        </div>
        <div class="w-full p-4 border border-1 border-white flex justify-evenly hover:bg-red-600 hover:text-white ease-in-out duration-300" data-scroll data-scroll-speed="-6" data-scroll-direction="horizontal" data-scroll-delay="1" >
            <p class="text-2xl text-white font-black text-center">UI & UX Design</p>
            <p class="text-2xl text-white font-black text-center">CREATIVE DIRECTION</p>
            <p class="text-2xl text-white font-black text-center">Product Design</p>
            <p class="text-2xl text-white font-black text-center">Blockchain</p>
            <p class="text-2xl text-white font-black text-center">Web Development</p>
        </div>
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
.skeww {
    position: absolute;
    /* transform: rotate(20deg) !important; */
}
</style>
