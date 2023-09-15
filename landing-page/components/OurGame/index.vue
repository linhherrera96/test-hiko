<template>
  <div class="ourgame-wrapper">
    <div class="col-12">
      <div class="col-12 d-flex text-center">
        <div class="ourgame-wrapper__pc">
          <div class="col-2"></div>
          <div class="col-8">
            <div class="mt-2 title">
              {{ $t("our_game") }}
            </div>
            <span class="info-content description">{{
              $t("our_game_text")
            }}</span>
          </div>
          <div class="col-2"></div>
        </div>
        <div class="ourgame-wrapper__mobile">
          <div class="col-12">
            <div class="mt-2 title">
              {{ $t("our_game") }}
            </div>
            <span class="info-content description">{{
              $t("our_game_text")
            }}</span>
          </div>
        </div>
      </div>
    </div>
    <div class="ourgame-wrapper__list">
      <div
        v-for="(item, index) in listProduct"
        :key="index"
        class="ourgame-wrapper__list--item"
      >
        <Card
          :name="item.name"
          :description="item.description"
          :image="item.image"
        ></Card>
      </div>
      <!-- <div class="row w-full ourgame-wrapper__item">
        <div v-for="(item, index) in listProduct" :key="index" class="col-3">
          <div class="ourgame">
            <Card
              :name="item.name"
              :description="item.description"
              :image="item.image"
            ></Card>
          </div>
        </div>
      </div> -->
    </div>
  </div>
</template>
<script>
import Card from "../Card";

export default {
  name: "OurGame",
  components: { Card },
  data() {
    return {
      listProduct: [
        {
          image: require("@/assets/images/ESpace.png"),
          name: "E-Space",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/Kingland.png"),
          name: "Kingland",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/LastGame.png"),
          name: "The Last Game",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/G-Dragon.png"),
          name: "G-Dragon",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/Pirates.png"),
          name: "Pirates",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/WitchParty.png"),
          name: "Witch Party",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/Rocky.png"),
          name: "Rocky",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/BlueFire.png"),
          name: "Blue Fire",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/MagicTree.png"),
          name: "Magic Tree",
          description:
            "TLorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/Aborigines.png"),
          name: "Aborigines",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/Cinderella.png"),
          name: "Cinderella",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          image: require("@/assets/images/EgyptGame.png"),
          name: "Egypt Game",
          description:
            "TLorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
      ],
    };
  },
};

import "@/assets/scss/ourgame.scss";
</script>
