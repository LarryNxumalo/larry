<template>
  <div id="app" class="relative">
     <div class="w-full h-full bg-black flex absolute">
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700"></div>
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700"></div>
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700"></div>
            <div class="bg-black w-1/4 h-full border-l border-r border-1 border-red-700"></div>
        </div>
    <div class="cursor-follower drop-shadow-2xl"></div>
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Section/>
 
 
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Section from './components/Section.vue'
// import Home from './components/Home.vue'
import gsap from 'gsap';
// import LocomotiveScroll from 'locomotive-scroll';

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Section,
    // Home,
  },
   data () {
    return {
      scroll: null
    }  
  },
    mounted() {
     this.setCursorAnimation()
  },
  beforeDestroy() {
    this.scroll.destroy()
  },
  methods: {
     setCursorAnimation() {
      /**
       * Mouse Follower (GSAP3)
       * Code by Blake Bowen
       * @link https://codepen.io/osublake/pen/dce29f9c14192035dbf55a32181f0bdc
       */
      // const gsap = this.$gsap
      const cursorFollower = document.querySelector('.cursor-follower')
      const pos = { x: window.innerWidth / 2, y: window.innerHeight / 2 }
      const mouse = { x: pos.x, y: pos.y }
      const speed = 0.13
      const fpms = 90 / 1000
      const xSet = gsap.quickSetter(cursorFollower, 'x', 'px')
      const ySet = gsap.quickSetter(cursorFollower, 'y', 'px')
      window.addEventListener('mousemove', e => {
        mouse.x = e.x
        mouse.y = e.y
        gsap.set('.cursor-follower', {
          opacity: 1,
          duration: 2,
          ease: 'expo.out'
        })
      })
      gsap.ticker.add((time, deltaTime) => {
        const delta = deltaTime * fpms
        const dt = 1.0 - Math.pow(1.0 - speed, delta)
        pos.x += (mouse.x - pos.x) * dt
        pos.y += (mouse.y - pos.y) * dt
        xSet(pos.x)
        ySet(pos.y)
      })
    }
  }
}
</script>
