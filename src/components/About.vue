<template>
  <div class="tokyo_tm_about">
    <div class="about_image">
      <!--<img src="" alt="" />-->
    </div>
    <!-- End .about_image -->

    <div class="description">
      <h3 class="name">Juan Camilo Niño Bermúdez</h3>
      <div class="description_inner">
        <div class="left">
          <p>
            Hola, mi nombre es Juan Camilo y soy programador web. Tengo 20 años y vivo en la ciudad de Bucaramanga, Santander. Me desempeño en la realización de sitios web hechos a medida (HTML - CSS - JS) y en la creación de páginas web mediante uso de CMS (Wordpress - Shopify - Drupal)
          </p>

        </div>
        <!-- End .left -->

        <div class="right">
          <ul>
            <li>
              <p><span>Cumpleaños:</span> 19.10.2001</p>
            </li>
            <li>
              <p><span>Edad:</span>20</p>
            </li>
            <li>
              <p><span>Ciudad:</span>Bucaramanga, Santander</p>
            </li>
            <li>
              <p>
                <span>Email:</span
                ><a href="mailto:mail@gmail.com">juannino863@gmail.com</a>
              </p>
            </li>
            <li>
              <p>
                <span>Phone:</span
                ><a href="tel:+770221770505">+57 310 222 8102</a>
              </p>
            </li>
            <li>
              <p><span>Estudios:</span>Programador Web | Universidad Nacional de Colombia</p>
            </li>
            <li>
              <p><span>Freelance:</span>Disponible</p>
            </li>
          </ul>
          <!-- End ul -->
        </div>
        <!-- End .right -->
      </div>
    </div>

    <!-- Start Modalbox -->
    <transition name="fade">
      <!-- Modal -->
      <div
        :class="{ 'modal-mask': isActive }"
        id="modal"
        @click="closeModal"
        v-if="isVisible"
      >
        <div
          class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-user"
          @click.stop
        >
          <div class="modal-content">
            <div class="tokyo_tm_modalbox_about">
              <div class="close" @click="closeModal">
                <img
                  class="svg"
                  src="../assets/img/svg/cancel.svg"
                  alt="cancel-img"
                />
              </div>
              <!-- End .close -->
              <div class="my_box">
                <div class="left">
                  <div class="about_title">
                    <h3>Habilidades</h3>
                  </div>
                  <!-- End .abut_title -->
                  <div class="tokyo_progress">
                    <div class="progress_inner">
                      <span
                        ><span class="label">Javascript</span
                        ><span class="number">95%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:95%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">PHP</span
                        ><span class="number">80%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:80%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">Frameworks (React - Angular - Next - Vue)</span
                        ><span class="number">90%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:90%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                  </div>
                  <!-- End .tokyo_progress -->
                </div>
                <!-- End .left -->
                <div class="right">
                  <div class="about_title">
                    <h3>idiomas</h3>
                  </div>
                  <div class="tokyo_progress">
                    <div class="progress_inner">
                      <span
                        ><span class="label">English</span
                        ><span class="number">95%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width:95%"></div>
                        </div>
                      </div>
                    </div>
                    <div class="progress_inner">
                    </div>
                    <div class="progress_inner">

                    </div>
                  </div>
                </div>
                <!-- End .right -->
              </div>
              <div class="counter">
                <div class="about_title">
                  <h3>Datos</h3>
                </div>
                <ul>
                  <li>
                    <div class="list_inner">
                      <h3>2021</h3>
                      <span>Desarrollador Web Universidad Nacional de Colombia</span>
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <h3>2022</h3>
                      <span>Desarrollador Jr en agencia Digital Premium</span>
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <h3>5</h3>
                      <span>Proyectos finalizados</span>
                    </div>
                  </li>
                </ul>
                <!-- End ul -->
              </div>
              <!-- End .counter -->
              <div class="partners">
                <div class="about_title">
                  <h3>Our Partners</h3>
                </div>
                <Brand />
              </div>
              <!-- End .partner -->
            </div>
            <!-- End .tokyo_tm_modalbox_about -->
          </div>
        </div>
      </div>
    </transition>
    <!-- End Modalbox -->
  </div>
</template>

<script>
import Brand from "./Brand";
export default {
  components: {
    Brand,
  },
  data() {
    return {
      isActive: false,
      isVisible: false,
    };
  },
  methods: {
    showModal: function() {
      this.isActive = true;
      this.isVisible = true;
    },
    closeModal: function() {
      this.isActive = false;
      this.isVisible = false;
    },
  },
};
</script>

<style lang="scss"></style>
