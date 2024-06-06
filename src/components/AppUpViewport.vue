<script>
// import HeaderComponent from "./components/Header.vue";

export default {
  data() {
    return {
      title: "titolo",
      scTimer: 0,
      scY: 0,
    };
  },
  methods: {
    handleScroll() {
      if (this.scTimer) return;
      this.scTimer = setTimeout(() => {
        this.scY = window.scrollY;
        clearTimeout(this.scTimer);
        this.scTimer = 0;
      }, 100);
    },
    toTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
};
</script>

<template>
  <!-- <div class="menu me-2 fw-bold">
    <div class="box card p-2 mb-2">
      <ul class="d-flex flex-column ps-0 my-auto">
        <li><font-awesome-icon icon="fa-solid fa-layer-group" size="xl" /></li>
        <li>Demos</li>
      </ul>
    </div>
    <div class="box p-2 card">
      <ul class="d-flex flex-column ps-0 my-auto">
        <li>
          <h3 class="mb-0">39</h3>
        </li>
        <li>On Sale</li>
      </ul>
    </div>
  </div> -->
  <div id="pagetop" :class="scY >= 400 ? 'o-100' : 'o-0'" @click="toTop">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="48"
      height="48"
      viewBox="0 0 24 24"
      fill="none"
      stroke="#4a5568"
      stroke-width="1"
      stroke-linecap="square"
      stroke-linejoin="arcs"
    >
      <path d="M18 15l-6-6-6 6" />
    </svg>
  </div>
</template>

<style lang="scss" scoped>
.box:hover {
  transform: scale(1.1);
}
.menu {
  display: flex;
  flex-direction: column;
  position: fixed;
  z-index: 6;
  right: 5px;
  top: 10%;
  h3 {
    color: #7abc64;
    font-weight: 900;
    &::before {
      content: "\0024";
      position: relative;

      top: -10px;
      font-size: 18px;
    }
  }
  & .box {
    box-shadow: 6px 11px 17px 0px #00000040;

    width: 100%;
    aspect-ratio: 1/1;
    text-align: center;
    transition: all 0.2s ease-in-out;
  }
}
.o-0 {
  opacity: 0%;
  z-index: -2;
}
.o-100 {
  opacity: 100%;
  z-index: 2;
}
#pagetop {
  position: fixed;
  bottom: 0;
  right: 0;
  transition: all 0.3s ease-in-out;
}
</style>
