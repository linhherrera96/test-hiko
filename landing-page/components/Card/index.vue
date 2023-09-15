<template>
  <div class="card">
    <img :src="image" alt="" class="w-100 image" />
    <div class="card__infomation">
      <p class="name">{{ name }}</p>
      <p class="description">
        {{ description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "card",
  props: ["image", "name", "description"],
};
</script>

<style lang="scss" scoped>
.card {
  @include screen(767) {
    height: 100%;
    width: 100%;
  }
  position: relative;
  cursor: pointer;
  transition: all 0.5s;
  &:hover {
    transform: scale(1.05);
    
  }
  .image {
    border-radius: 5px;
    @include screen(767) {
      height: 100%;
    width: 100%;
    }
  }

  &__infomation {
    position: absolute;
    bottom: 0;
    left: 0;
    padding: 0 32px 44px;
    @include screen(767) {
      bottom: 0;
      left: 0;
      padding: 0 18px 10px 8px;
    }
    .name {
      font-weight: 700;
      font-size: 48px;
      line-height: 60px;
      letter-spacing: 1px;
      color: #fffdf1;
      padding-right: 20px;
      width: 100%;
      @include screen(767) {
        padding-right: 0;
        font-size: 24px;
        line-height: 19px;
      }
    }

    .description {
      font-size: 12px;
      color: #fff;
      margin-bottom: 0;
      @include screen(767) {
        bottom: 0;
        left: 0;
        font-size: 12px;
        line-height: 16px;
        letter-spacing: 1px;
        color: #fff;
        margin-bottom: 0;
      }
    }
  }
}
</style>
