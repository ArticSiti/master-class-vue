<template>
  <div class="home">
    <banner></banner>
    <div class="result">
      <matches
        :pastTitle="pastTitle"
        :imgUrl="imgUrl"
        :description="description"
        :buttonDescritpion="buttonDescritpion"
      ></matches>
      <matches
        :newTitle="newTitle"
        :imgUrl="imgUrl"
        :style="style"
        :description="description"
        :buttonDescritpion="buttonDescritpion"
      ></matches>
    </div>
  </div>
</template>
<script>
import Banner from "@/components/banner";
import Matches from "@/components/descriptionMatches";
export default {
  name: "Home",
  components: {
    Banner,
    Matches,
  },
  data() {
    return {
      pastTitle: "Прошедшие матчи",
      newTitle: "Предстоящие матчи",
      description: "Отчёт о матче",
      buttonDescritpion: "Ключевые моменты",

      imgUrl: [
        require("@/assets/img/ef817c2bd6f16a9b6f36b97a3c53e9d8.jpg"),
        require("@/assets/img/f8de226d8ba9ac40783029887b1bfe54.jpeg"),
        require("@/assets/img/kartinki24_ru_country_flags_82.jpg"),
      ],
    };
  },
};
</script>
<style>
.result {
  display: flex;
}
.disabled {
  background: #bdbdbd;
}
</style>
