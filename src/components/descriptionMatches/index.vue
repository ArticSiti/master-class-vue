<template>
  <div class="matches container">
    <div class="matches-block">
      <div class="matches-block__title">
        <h2 v-if="this.pastTitle">{{ pastTitle }}</h2>
        <h2 v-if="this.newTitle">{{ newTitle }}</h2>
      </div>
      <!-- Передаём названия из родительского компонента -->
      <div class="matches-block__card">
        <div class="matches-block__left">
          <div class="matches-block__wrapper">
            <div class="matches-block__contain">
              <div class="matches-block__images">
                <div class="matches-block__images-contain">
                  <img v-if="this.pastTitle" :src="imgUrl[0]" alt="" />
                  <img v-if="this.newTitle" :src="imgUrl[2]" alt="" />
                </div>
                <!-- Передаём картинки из родительского -->
              </div>
              <div class="matches-block__description">
                <button v-if="this.pastTitle" class="matches-block__button btn">
                  {{ description }}
                </button>
                <!-- Передаём описание кнопки -->
                <button
                  v-if="this.newTitle"
                  class="matches-block__button btn disabled"
                  :disabled="disabled"
                >
                  {{ description }}
                </button>
                <!-- Передаём описание кнопки -->
              </div>
            </div>
          </div>
        </div>
        <div v-if="this.pastTitle" class="matches-block__check">
          <h3>1</h3>
          <span>:</span>
          <h3>2</h3>
        </div>
        <div v-if="this.newTitle" class="matches-block__check">
          <h3>-</h3>
          <span>:</span>
          <h3>-</h3>
        </div>
        <div class="matches-block__right">
          <div class="matches-block__wrapper">
            <div class="matches-block__contain">
              <div class="matches-block__images">
                <div class="matches-block__images-contain">
                  <img v-if="this.pastTitle" :src="imgUrl[1]" alt="" />
                  <img v-if="this.newTitle" :src="imgUrl[1]" alt="" />
                </div>
              </div>
              <div class="matches-block__description moments">
                <button class="matches-block__button btn">
                  {{ buttonDescritpion }}
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "DescriptionMatches",
  props: {
    pastTitle: String,
    newTitle: String,
    imgUrl: Array,
    style: String,
    description: String,
    buttonDescritpion: String,
  },
};
</script>
<style lang="scss" scoped>
.matches {
  margin-top: 33px;
  &-block {
    &__title {
      text-align: center;
      h2 {
        font-size: 32px;
      }
    }
    &__card {
      display: flex;
      margin-top: 25px;
    }
    &__images {
      display: flex;
      justify-content: center;
      width: 100%;
      height: 78px;
      overflow: hidden;

      img {
        width: 100%;
        height: 100%;
        border-radius: 5px;
        object-fit: cover;
      }
    }
    &__check {
      display: flex;
      align-items: center;
      height: 80px;
      h3 {
        font-size: 32px;
        font-family: "SF Light";
        margin: 0px 15px 0px 15px;
      }
    }
    &__description {
      margin-top: 8px;
    }
    &__button {
      border: none;
      padding: 6px 31px;
      &:hover {
        cursor: pointer;
      }
    }
  }
}
.moments {
  .btn {
    background: none;
    border: 1px solid gray;
    color: #000;
  }
}
</style>
