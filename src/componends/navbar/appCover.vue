<template>
  <div class="appCover-container">
    <div class="text_box">
      <h1>倾心FM</h1>
    </div>
    <div class="text_box2">
      <!--<h1>世界和我爱着你</h1>-->
      <h1>你是我的心中挚爱</h1>
    </div>
    <div class="longBox">
      <div class="bar bar1"></div>
      <div class="bar bar2"></div>
      <div class="bar bar3"></div>
      <div class="bar bar4"></div>
      <div class="bar bar5"></div>
      <div class="bar bar6"></div>
      <div class="bar bar7"></div>
      <div class="bar bar8"></div>
    </div>
  </div>
</template>

<script>
export default {
  created() {
    this.goHomePage();
  },
  methods: {
    goHomePage() {
      this.$store.commit("setFooterShow", false);
      setTimeout(() => {
        this.$router.push({path: '/login', replace: true})
        // this.$router.push("/login");
      }, 3000);
    }
  }
};
</script>

<style lang="scss" scoped>
.appCover-container {
  z-index: 99;
  position: relative;
  top: 0;
  left: 0;
  font-size: 1.5rem;
  height: 100%;
  background: url("https://img.alicdn.com/imgextra/i1/790237325/O1CN016XDOHK23ytmGbVGEM_!!790237325.jpg?t=1587200350000");
  background-size: 100% 100%;
  .text_box {
    position: absolute;
    top: 5rem;
    left: 0.5rem;
  }
  .text_box2 {
    position: absolute;
    top: 7.5rem;
    right: 0.5rem;
  }

  h1 {
    font-family: "STXingkai", "YouYuan", "Microsoft YaHei", "宋体", sans-serif;
    font-weight: 800;
    color: #2c3e5036;
    line-height: 1.1;
    background: url("https://img.alicdn.com/imgextra/i4/790237325/O1CN01kpk1pG23ytmCJ9aF1_!!790237325.png?t=1587200371000");
    -webkit-background-clip: text;
    background-position: 0 18%;
    animation: water 12s infinite;
  }
  @keyframes water {
    from {
      background-position: left 0 top 18%;
    }
    to {
      background-position: left 800px top 18%;
    }
  }

  .longBox {
    position: absolute;
    bottom: 1rem;
    right: 1rem;
    .bar {
      display: inline-block;
      width: 0.2rem;
      height: 2rem;
      background-color: rgba(48, 48, 83, 0.3);
      transform-origin: bottom center;
      animation: loading 1.5s ease-in-out infinite;
    }
    .bar1 {
      animation-delay: 0.1s;
    }

    .bar2 {
      animation-delay: 0.2s;
    }

    .bar3 {
      animation-delay: 0.3s;
    }

    .bar4 {
      animation-delay: 0.4s;
    }

    .bar5 {
      animation-delay: 0.5s;
    }

    .bar6 {
      animation-delay: 0.6s;
    }

    .bar7 {
      animation-delay: 0.7s;
    }

    .bar8 {
      animation-delay: 0.8s;
    }

    @keyframes loading {
      0% {
        transform: scaleY(0.1);
        background-color: rgb(47, 70, 172);
      }

      50% {
        transform: scaleY(1);
        background-color: #5761bd;
      }

      100% {
        transform: scaleY(0.1);
        background-color: transparent;
      }
    }
  }
}
</style>