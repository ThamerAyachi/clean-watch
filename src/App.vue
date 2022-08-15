<template>
  <div>
    <NavBar></NavBar>
    <div class="flex justify-center">
      <div class="lg:w-3/5 md:w-4/5 mx-5">
        <div
          class="flex justify-between text-gray-400 items-center md:items-end"
        >
          <p class="md:text-3xl text-xl tagline">Find your great watch</p>
          <p><span class="text-black text-5xl font-bold">2</span>/21</p>
        </div>

        <div class="gray text-center font-semibold uppercase">Gray</div>

        <div class="grid sm:grid-cols-2">
          <!-- button -->
          <div class="flex justify-center items-center">
            <button
              class="bg-black text-white text-xl px-6 py-2 rounded-lg mb-4 more"
            >
              show more watches
            </button>
          </div>

          <div class="desc">
            <p class="text-3xl my-3">
              Your <span class="text-lime-400">heathy</span> life <br />
              start here with us
            </p>
            <p class="sm:hidden">
              A family owned company founded with the purpose of giving your
              family access to clean, organic products while you are on the go.
            </p>
          </div>
        </div>

        <!-- watch -->
        <div class="watch">
          <img src="/img/watch-removebg-preview.png" alt="" />
        </div>

        <!-- leaves -->
        <div class="leaves">
          <ul id="scene">
            <li class="layer" data-depth="-.1">
              <img src="/img/leaf01.png" alt="" />
            </li>
            <li class="layer" data-depth="-.3">
              <img src="/img/leaf02.png" alt="" />
            </li>
            <li class="layer" data-depth="-1.5">
              <img src="/img/leaf03.png" alt="" />
            </li>
            <li class="layer" data-depth=".1">
              <img src="/img/leaf04.png" alt="" />
            </li>
            <li class="layer" data-depth=".3">
              <img src="/img/leaf05.png" alt="" />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Parallax from "parallax-js";
import gsap from "gsap";

import NavBar from "./components/NavBar.vue";

export default {
  name: "App",
  components: {
    NavBar,
  },
  mounted() {
    var scene = document.getElementById("scene");
    new Parallax(scene);

    gsap.from(".watch", 1, {
      opacity: 0,
      y: -800,
      delay: 1,
    });

    gsap.from(".leaves .layer:nth-child(1)", 2, {
      delay: 1,
      opacity: 0,
      y: -800,
    });
    gsap.from(".leaves .layer:nth-child(2)", 2, {
      delay: 1.3,
      opacity: 0,
      y: -800,
    });
    gsap.from(".leaves .layer:nth-child(3)", 2, {
      delay: 1.4,
      opacity: 0,
      y: -800,
    });
    gsap.from(".leaves .layer:nth-child(4)", 2, {
      delay: 1.5,
      opacity: 0,
      y: -800,
    });
    gsap.from(".leaves .layer:nth-child(5)", 2, {
      delay: 1.6,
      opacity: 0,
      y: -800,
    });

    gsap.from(".gray", 1, {
      delay: 1,
      opacity: 0,
      y: 20,
    });

    gsap.from(".tagline", 1, {
      delay: 1.3,
      opacity: 0,
      y: 20,
    });

    gsap.from(".pages", 1, {
      delay: 1.3,
      opacity: 0,
      y: 20,
    });

    gsap.from(".more", 1, {
      delay: 1.4,
      opacity: 0,
      y: 20,
    });

    gsap.from(".desc", 1, {
      delay: 1.4,
      opacity: 0,
      y: 20,
    });
  },
};
</script>

<style></style>
