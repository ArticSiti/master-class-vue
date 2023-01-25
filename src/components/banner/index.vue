<template>
  <div class="banner">
    <div class="banner-container">
      <div class="banner-container__block">
        <div class="banner-container__description container">
          <h3>
            АНГЛИЯ ВЫБЫВАЕТ ИЗ ЧЕМПИОНАТА МИРА ПОСЛЕ ПОРАЖЕНИЯ ОТ СБОРНОЙ
            ФРАНЦИИ
          </h3>
          <div class="button">
            <button class="button_hover btn">УЗНАТЬ БОЛЬШЕ</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script></script>
<style lang="scss" scoped>
.banner {
  background-image: url(@/assets/img/kieran-trippier.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  height: 100vh;
  &-container {
    &__block {
      margin-left: 100px;
    }
    &__description {
      position: absolute;
      margin-top: 141px;
      width: 400px;
      padding: 32px;
      border-radius: 5px;
      h3 {
        color: #fff;
        font-size: 32px;
        font-family: 'SF Bold';
      }
      background: #000;
    }
  }
}
.button{
    margin-top: 107px;
    display: flex;
    justify-content: center;
    &_hover{
        transition: .3s;
    }
}
.button:hover .button_hover{
    background: #7a9bf0;
    cursor: pointer;
}
</style>
