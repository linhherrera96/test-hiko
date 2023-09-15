<template>
  <div class="timeline" @scroll="onScroll(event)">
    <div class="timeline-banner">
      <div class="title">
        <span class="title-countdown">{{ $t("toppage.getting_ready") }}</span>
        <div class="justify-content-center">
          <div class="countdown">
            <div class="time">
              <div class="pt-4 px-4 justify-content-center d-flex">
                <div class="block">
                  <p class="digit">{{ times[0].time }}</p>
                  <p class="text">{{ $t("toppage.day") }}</p>
                </div>

                <div class="block">
                  <p class="digit">:</p>
                </div>
                <div class="block">
                  <p class="digit">{{ times[1].time }}</p>
                  <p class="text">{{ $t("toppage.hour") }}</p>
                </div>
                <div class="block">
                  <p class="digit">:</p>
                </div>
                <div class="block">
                  <p class="digit">{{ times[2].time }}</p>
                  <p class="text">{{ $t("toppage.minute") }}</p>
                </div>
                <div class="block">
                  <p class="digit">:</p>
                </div>
                <div class="block">
                  <p class="digit">{{ times[3].time }}</p>
                  <p class="text">{{ $t("toppage.second") }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="introduction">
          <span class="d-flex introduction__text">
            {{ $t("toppage.sign_up_text") }}
          </span>
          <b-input-group>
            <b-form-input
              class="input-search"
              :placeholder="$t('email_placeholder')"
            ></b-form-input>
            <b-input-group-append>
              <img
                class="input-icon"
                src="@/assets/images/IconArrowNext.svg"
                alt=""
              />
            </b-input-group-append>
          </b-input-group>
        </div>
      </div>
      <img
        src="@/assets/images/background.png"
        alt=""
        class="img-fluid background-banner"
      />
      <img
        src="@/assets/images/background_mobile.png"
        alt=""
        class="img-fluid background-banner-mobile"
      />
    </div>
  </div>
</template>
<script>
export default {
  name: "Product",
  data() {
    return {
      startTime: "September 17, 2023 14:09:00",
      endTime: "September 23, 2023 14:10:00",
      times: [
        { id: 0, text: "Days", time: 1 },
        { id: 1, text: "Hours", time: 1 },
        { id: 2, text: "Minutes", time: 1 },
        { id: 3, text: "Seconds", time: 1 },
      ],
      timeinterval: undefined,
    };
  },

  created() {
    this.updateTimer();
    this.timeinterval = setInterval(this.updateTimer, 1000);
  },

  methods: {
    goToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth",
      });
    },

    updateTimer() {
      if (
        this.times[3].time > 0 ||
        this.times[2].time > 0 ||
        this.times[1].time > 0 ||
        this.times[0].time > 0
      ) {
        this.getTimeRemaining();
      } else {
        let nextStartTime = parseInt(this.endTime.slice(15, 17));
        let nextEndTime = parseInt(this.endTime.slice(15, 17)) + 5;
        this.startTime = `March 10, 2030 ${nextStartTime}:36:00`;
        this.endTime = `March 10, 2030 ${nextEndTime}:37:00`;
        this.getTimeRemaining();
      }
    },

    getTimeRemaining() {
      let t = Date.parse(new Date(this.endTime)) - Date.parse(new Date());
      if (t >= 0) {
        this.times[3].time = Math.floor((t / 1000) % 60); //seconds
        this.times[2].time = Math.floor((t / 1000 / 60) % 60); //minutes
        this.times[1].time = Math.floor((t / (1000 * 60 * 60)) % 24); //hours
        this.times[0].time = Math.floor(t / (1000 * 60 * 60 * 24)); //days
      } else {
        this.times[3].time =
          this.times[2].time =
          this.times[1].time =
          this.times[0].time =
            0;
      }
    },
  },
};

import "@/assets/scss/timeline.scss";
</script>
