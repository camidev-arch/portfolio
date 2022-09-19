<template>
  <div>
    <!-- Start leftpart -->
    <div class="leftpart">
      <div class="leftpart_inner">
        <div class="logo">
          <router-link to="/"
            ><img style="filter: invert(0) !important;" src="../assets/img/logo/JNK.png" alt=""
          /></router-link>
        </div>
        <!-- End .logo -->
        <div class="menu">
          <a
            v-on:click="activetab = 1"
            :class="[activetab === 1 ? 'active' : '']"
          >
            <img
              class="svg"
              src="../assets/img/svg/home-run.svg"
              alt="homerun"
            />
            <span class="menu_content">Inicio</span></a
          >
          <!-- End Home -->
          <a
            v-on:click="activetab = 2"
            :class="[activetab === 2 ? 'active' : '']"
          >
            <img class="svg" src="../assets/img/svg/avatar.svg" alt="avatar" />
            <span class="menu_content">Sobre mi</span></a
          >
          <!-- End About -->
          <a
            v-on:click="activetab = 3"
            :class="[activetab === 3 ? 'active' : '']"
          >
            <img
              class="svg"
              src="../assets/img/svg/briefcase.svg"
              alt="briefcase"
            />
            <span class="menu_content">Portafolio</span></a
          >
          <!-- End Portfolio -->

          <!-- End News -->

          <!-- End Contact -->
        </div>
        <div class="copyright">
          <p>
            &copy; {{ new Date().getFullYear() }} JNKREATIONS<br />Desarrollado por
            <a
              href="https://themeforest.net/user/ib-themes"
              target="_blank"
              rel="noreferrer"
            >
              Juan Niño
            </a>
          </p>
        </div>
        <!-- End copyright -->
      </div>
    </div>
    <!-- End leftpart -->

    <!-- Start rightpart -->
    <div class="rightpart">
      <div class="rightpart_in">
        <div class="tokyo_tm_section">
          <div class="container">
            <div v-if="activetab === 1" class="tabcontent">
              <Home />
            </div>
            <!-- End Home tabcontent -->
            <div v-if="activetab === 2" class="tabcontent">
              <About />
            </div>
            <!-- End About tabcontent  -->
            <div v-if="activetab === 3" class="tabcontent">
              <Portfolio />
            </div>
            <!-- End Portfolio tabcontent -->
            <div v-if="activetab === 4" class="tabcontent">
              <News />
            </div>
            <!-- End News tabcontent -->
            <div v-if="activetab === 5" class="tabcontent">
              <Contact />
            </div>
            <!-- End Contact tabcontent -->
          </div>
        </div>
      </div>
    </div>
    <!-- End rightpart -->
  </div>
</template>

<script>
  import Home from "../components/Home";
  import About from "../components/About";
  import Portfolio from "../components/Portfolio";
  import News from "../components/News";
  import Contact from "../components/Contact";
  export default {
    components: {
      Home,
      About,
      Portfolio,
      News,
      Contact,
    },
    data() {
      return {
        activetab: 1,
      };
    },
  };
</script>

<style lang="scss" scoped></style>
