<template>
  <div>
    <div class="footer col-12">
      <b-col class="logo" md="5" sm="12">
        <div>
          <img src="@/assets/images/Logo.svg" alt="" class="footer-logo" />
        </div>
        <div class="linked">
          <img src="@/assets/images/twiter.svg" alt="" class="footer-logo" />
          <img src="@/assets/images/facebook.svg" alt="" class="footer-logo" />
          <img src="@/assets/images/ins.svg" alt="" class="footer-logo" />
        </div>
      </b-col>
      <b-col class="info" md="4" sm="12">
        <div class="title">{{ $t("address") }}</div>
        <div class="mt-3 d-flex align-items-center">
          <img src="@/assets/images/location.png" alt="" class="icon" />
          <div class="d-block ml-2">
            <span class="description d-flex"
              >Valletta Buildings, South Street, Valletta - VLT 1103 Malta,
              US</span
            >
            <span class="description"
              >20 Phan Dang Luu street, Hai Chau District, Danang city,
              Vietnam</span
            >
          </div>
        </div>
        <div class="mt-3 d-flex align-items-center">
          <img src="@/assets/images/mobile.png" alt="" class="icon" />
          <span class="description ml-2"
            >(+1) 555-0108-000 or (+236) 555-0108</span
          >
        </div>
      </b-col>
      <b-col class="subscribe" md="3" sm="12">
        <div class="title">{{ $t("subscribe") }}</div>
        <div class="mt-3 d-flex align-items-center">
          <div class="d-block">
            <span class="description d-flex">{{ $t("subscribe_text") }}</span>
            <b-input-group>
              <b-form-input
                class="input-search mt-3"
                placeholder="Email"
              ></b-form-input>
              <b-input-group-append>
                <img
                  class="input-icon"
                  src="@/assets/images/arrow-right.png"
                  alt=""
                />
              </b-input-group-append>
            </b-input-group>
          </div>
          <div class="mt-3 d-flex align-items-center"></div>
        </div>
      </b-col>
    </div>
    <div class="d-flex text-center">
      <div class="footer-copyright">2017 Copyright. Policy.</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};

import "@/assets/scss/footer.scss";
</script>
