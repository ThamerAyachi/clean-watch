<template>
  <div>
    <div class="flex justify-between uppercase py-6 px-6 menu-links">
      <div class="font-semibold lg:text-4xl text-2xl logo">Clean Watch</div>

      <ul class="lg:flex font-semibold text-sm space-x-6 items-center hidden">
        <li>location</li>
        <li>our store</li>
        <li>contact us</li>
      </ul>

      <ul class="lg:flex font-semibold space-x-6 items-center hidden">
        <li class=""><i class="fa fa-search search"></i></li>
        <li class="text-sm"><span class="account"> my account</span></li>
        <li><i class="fa fa-shopping-cart cart"></i></li>
      </ul>

      <div class="flex items-center lg:hidden"><i class="fa fa-bars"></i></div>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";

export default {
  mounted() {
    gsap.from(".logo", 1, { opacity: 0, x: -20 });
    gsap.from(
      ".menu-links ul li",
      1,
      {
        opacity: 0,
        x: -20,
      },
      0.08
    );
    gsap.from(".search", 1, {
      delay: 0.5,
      opacity: 0,
      x: -20,
    });

    gsap.from(".account", 1, {
      delay: 0.6,
      opacity: 0,
      x: -20,
    });

    gsap.from(".cart", 1, {
      delay: 0.7,
      opacity: 0,
      x: -20,
    });
  },
};
</script>

<style lang="scss" scoped></style>
