<template>
  <div class="header">
    <b-container fluid>
      <div class="header-toppage">
        <b-navbar toggleable="lg" type="dark" class="d-flex">
          <b-navbar-toggle
            target="nav-collapse"
            v-on:click="toggleMenu"
          ></b-navbar-toggle>
          <img src="@/assets/images/Logo.svg" alt="" class="logo" />
          <b-collapse class="nav-item justify-content-end text-white" is-nav>
            <b-navbar-nav class="px-4 mr-3">
              <b-nav-item href="#">{{ $t("toppage.about_us") }}</b-nav-item>
            </b-navbar-nav>
            <b-navbar-nav class="px-4 mr-3">
              <b-nav-item href="#">{{ $t("toppage.games") }}</b-nav-item>
            </b-navbar-nav>
            <b-navbar-nav class="px-4 mr-3">
              <b-nav-item href="#">{{ $t("toppage.partners") }}</b-nav-item>
            </b-navbar-nav>
            <b-navbar-nav class="px-4 mr-3">
              <b-nav-item href="#">{{ $t("toppage.contact_us") }} </b-nav-item>
            </b-navbar-nav>
            <!-- Right aligned nav items -->
          </b-collapse>
          <div v-if="isMenu" class="menu d-flex justify-content-center">
            <div class="d-flex header">
              <div class="dropdown mt-3 ml-3">
                <div class="dropbtn">
                  <img
                    v-if="$i18n.locale === 'en'"
                    src="@/assets/images/united-states.png"
                    alt=""
                  />
                  <img
                    v-else
                    src="@/assets/images/vietnam.png"
                    alt=""
                  /><span></span>
                </div>
                <div class="dropdown-content">
                  <div class="ml-2 d-flex">
                    <img
                      v-if="$i18n.locale === 'vi'"
                      src="@/assets/images/tick.svg"
                      alt=""
                    />
                    <span v-else style="width: 23px"></span>
                    <p
                      v-on:click="changeLang('vi')"
                      class="mt-2 mb-2 ml-2 font-weight-bold"
                    >
                      <img src="@/assets/images/vietnam.png" alt="" /><span
                        class="ml-2"
                        >Vietnamese
                      </span>
                    </p>
                  </div>
                  <div style="border: 1px solid #c4c4c4"></div>
                  <div class="ml-2 d-flex">
                    <img
                      v-if="$i18n.locale === 'en'"
                      src="@/assets/images/tick.svg"
                      alt=""
                    />
                    <span v-else style="width: 23px"></span>
                    <p
                      v-on:click="changeLang('en')"
                      class="mt-2 mb-2 ml-2 font-weight-bold"
                    >
                      <img
                        src="@/assets/images/united-states.png"
                        alt=""
                      /><span class="ml-2">English</span>
                    </p>
                  </div>
                </div>
              </div>
              <div v-on:click="onClose">
                <img src="@/assets/images/close.png" class="mr-3" alt="" />
              </div>
            </div>
            <div class="nav-item">
              <p>{{ $t("toppage.about_us") }}</p>
              <p class="nav-item__title">{{ $t("toppage.games") }}</p>
              <p class="nav-item__title">{{ $t("toppage.partners") }}</p>
              <p class="nav-item__title">{{ $t("toppage.contact_us") }}</p>
            </div>
          </div>
          <div class="d-flex justify-content-center">
            <div class="dropdown">
              <button class="dropbtn">
                <img
                  v-if="$i18n.locale === 'en'"
                  src="@/assets/images/united-states.png"
                  alt=""
                />
                <img
                  v-else
                  src="@/assets/images/vietnam.png"
                  alt=""
                /><span></span>
              </button>
              <div class="dropdown-content">
                <div class="ml-2 d-flex">
                  <img
                    v-if="$i18n.locale === 'vi'"
                    src="@/assets/images/tick.svg"
                    alt=""
                  />
                  <span v-else style="width: 23px"></span>
                  <p
                    v-on:click="changeLang('vi')"
                    class="mt-2 mb-2 ml-2 font-weight-bold"
                  >
                    <img src="@/assets/images/vietnam.png" alt="" /><span
                      class="ml-2"
                      >Vietnamese
                    </span>
                  </p>
                </div>
                <div style="border: 1px solid #c4c4c4"></div>
                <div class="ml-2 d-flex">
                  <img
                    v-if="$i18n.locale === 'en'"
                    src="@/assets/images/tick.svg"
                    alt=""
                  />
                  <span v-else style="width: 23px"></span>
                  <p
                    v-on:click="changeLang('en')"
                    class="mt-2 mb-2 ml-2 font-weight-bold"
                  >
                    <img src="@/assets/images/united-states.png" alt="" /><span
                      class="ml-2"
                      >English</span
                    >
                  </p>
                </div>
              </div>
            </div>
          </div>
        </b-navbar>
      </div>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      isMenu: false,
    };
  },

  methods: {
    changeLang(lang) {
      this.$i18n.locale = lang;
    },

    toggleMenu() {
      this.isMenu = true;
    },

    onClose() {
      this.isMenu = false;
    },
  },
};

import "@/assets/scss/header.scss";
</script>
