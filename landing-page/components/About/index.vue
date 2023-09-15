<template>
  <div class="mt-5">
    <div class="about-us-wrapper">
      <div class="col-12">
        <div class="row about-us-content">
          <div class="col-md-4 about-us-content__left">
            <span class="about-us-content__title">
              {{ $t("about.about_us") }}</span
            >
            <span class="about-us-content__description">{{
              $t("about.about_content")
            }}</span>
            <div class="about-us-content__around">
              <div class="about-us-content__user">
                <div class="d-flex">
                  <span class="number">600</span>
                  <span class="number-text">M</span>
                  <span class="number">+</span>
                </div>
                <span class="text">{{ $t("about.about_users") }}</span>
              </div>
              <div class="about-us-content__game">
                <div class="d-flex">
                  <span class="number">135</span>
                  <span class="number-text">M</span>
                  <span class="number">+</span>
                </div>
                <span class="text">{{ $t("about.about_games") }}</span>
              </div>
            </div>
          </div>
          <div class="col-md-4 about-us-content__right d-flex">
            <div class="m-auto">
              <div class="d-flex p-3 mb-4">
                <div class="col-2">
                  <img
                    class="about-image"
                    src="@/assets/images/calendar-tick.svg"
                    alt=""
                  />
                  <img src="@/assets/images/Oval.svg" alt="" />
                </div>
                <div class="col-10">
                  <span class="about-us d-block">{{
                    $t("about.about_hour")
                  }}</span>
                  <span>{{ $t("about.about_hour_text") }}</span>
                </div>
              </div>
              <div class="d-flex p-3">
                <div class="col-2">
                  <img
                    class="about-image"
                    src="@/assets/images/pen-tool-2.svg"
                    alt=""
                  />
                  <img src="@/assets/images/Oval.svg" alt="" />
                </div>
                <div class="col-10">
                  <span class="about-us d-block">{{
                    $t("about.about_design")
                  }}</span>
                  <span>{{ $t("about.about_design_text") }}</span>
                </div>
              </div>
              <div class="d-flex p-3">
                <div class="col-2">
                  <img
                    class="about-image"
                    src="@/assets/images/people.svg"
                    alt=""
                  />
                  <img src="@/assets/images/Oval.svg" alt="" />
                </div>
                <div class="col-10">
                  <span class="about-us d-block">{{
                    $t("about.about_team")
                  }}</span>
                  <span>{{ $t("about.about_team_text") }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="about-introduction container">
      <div class="about-introduction__image">
        <img src="@/assets/images/Illustrator.png" alt="" class="img-fluid" />
      </div>
      <img src="@/assets/images/map.png" alt="" class="map-image img-fluid" />
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};

import "@/assets/scss/about.scss";
</script>
