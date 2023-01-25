<template>
  <div class="menu">
  <nav class="nav">
    <div class="top-menu">
      <div class="top-menu__wrapper container">
        <div class="top-menu__wrapper_end">
          <router-link to="/home">Главная</router-link>
          <router-link to="/news">Новости</router-link>
          <router-link to="/matches">Матчи</router-link>
          <router-link to="/tv">TV</router-link>
          <router-link to="/tickets">Билеты</router-link>
          <router-link to="/teams">Команды</router-link>
        </div>
      </div>
    </div>
  </nav>
  <router-view />
</div>
</template>

<style lang="scss">
.top-menu {
  position: fixed;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  &__wrapper {
    display: flex;
    justify-content: flex-end;
    padding: 18px 0px 18px;
    &_end {
      a {
        margin-left: 60px;
        text-decoration: none;
        font-size: 20px;
        color: #fff;
        font-weight: bold;
      }
    }
  }
}
</style>
