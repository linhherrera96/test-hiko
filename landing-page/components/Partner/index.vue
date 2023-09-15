<template>
  <div class="partner-wrapper">
    <div class="container">
      <div class="container info">
        <div class="title mt-2 text-title">{{ $t("out_partner") }}</div>
        <div class="col-12 partner-list">
          <div class="d-flex justify-content-center align-items-center">
            <VueSlickCarousel v-bind="settings">
              <div
                v-for="(item, index) in listPartner"
                :key="index"
                class="d-flex"
              >
                <img :src="item.image" alt="" class="partner-logo" />
              </div>
            </VueSlickCarousel>
          </div>
        </div>
      </div>
    </div>
    <a class="bottom-right" @click="goToTop()" v-if="isUserScrolling"
      ><img
        src="@/assets/images/arrow-circle-up.png"
        class="rotate-icon"
        alt=""
      />
    </a>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
export default {
  name: "Product",
  components: { VueSlickCarousel },
  data() {
    return {
      listPartner: [
        {
          image: require("@/assets/images/Rectangle 52.png"),
        },
        {
          image: require("@/assets/images/Rectangle 53.png"),
        },
        {
          image: require("@/assets/images/Rectangle 54.png"),
        },
        {
          image: require("@/assets/images/Rectangle 55.png"),
        },
        {
          image: require("@/assets/images/Rectangle 56.png"),
        },
        {
          image: require("@/assets/images/Rectangle 62.png"),
        },
        {
          image: require("@/assets/images/Rectangle 63.png"),
        },
      ],

      isUserScrolling: false,
      settings: {
        infinite: false,
        speed: 500,
        slidesToShow: 5,
        slidesToScroll: 2,
        initialSlide: 0,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              slidesToShow: 5,
              slidesToScroll: 5,
              infinite: true,
              dots: true,
            },
          },
          {
            breakpoint: 600,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 2,
              initialSlide: 2,
            },
          },
          {
            breakpoint: 480,
            settings: {
              slidesToShow: 1,
              slidesToScroll: 1,
            },
          },
        ],
      },
    };
  },

  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },

  methods: {
    goToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth",
      });
    },

    handleScroll(event) {
      // Any code to be executed when the window is scrolled
      this.isUserScrolling = window.scrollY > 0;
    },
  },
};

import "@/assets/scss/partner.scss";
</script>
