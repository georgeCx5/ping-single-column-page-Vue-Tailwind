<script>
import PlatformManager from './components/PlatformManager.vue';
import dashboardImg from '@/assets/images/illustration-dashboard.png'

export default {
  data() {
    return {
      emailRgx: new RegExp(/^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/),
      dashboardImg,
      logoImg: 'bg-[url("@/assets/images/logo.svg")]',
    }
  },
  components: {
    PlatformManager,
  }
}
</script>
<template>
  <body class="  font-franklin">
    <main class=" flex flex-col items-center">
      <div :class="`${logoImg} w-[56px] h-[17px] bg-contain`"></div>
      <h1 class=" text-[22px] leading-[32px] text-neo-gray font-light">We are launching
        <span class=" text-neo-dark font-bold">soon!</span>
      </h1>
      <p class=" text-neo-dark text-[12px] leading-[15px] font-light">Subscribe and get notified</p>
      <div class=" w-[282px]">
        <input
          class=" w-full h-[40px] px-8 text-neo-pale-blue text-[12px] leading-[20px] outline outline-1 outline-neo-pale-blue rounded-[28px]"
          type="email">
        <button class=" w-full h-[40px] bg-neo-blue text-white text-[12px] leading-[16px] font-semibold rounded-[28px]"
          type="submit">Notify Me</button>
      </div>
      <img class=" w-[320px]" :src="dashboardImg" alt="dashboardImg">
    </main>
    <footer class=" flex flex-col items-center">
      <h3 class=" text-neo-gray text-[10px] leading-[12px]">&copy; Copyright Ping. All rights reserved.</h3>
      <div class=" flex gap-3">
        <PlatformManager platform="facebook" />
        <PlatformManager platform="twitter" />
        <PlatformManager platform="instagram" />
      </div>
    </footer>
  </body>
</template>