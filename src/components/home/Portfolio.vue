<template>
  <div class="portfolio">
    <title-header :title="'Take Flight'" class="mb-5" />
    <div class="row col-lg-10">
      <div
        class="col-md-6 col-sm-12 col-lg-4"
        v-for="(card, index) in cards"
        :key="index"
      >
        <double-bordered-card :title="card.title" :routes="card.routes" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import TitleHeader from "./TitleHeader";
import DoubleBorderedCard from "./DoubleBorderedCard.vue";
export default {
  components: { DoubleBorderedCard, TitleHeader },
  setup() {
    const cards = ref([
      {
        title: "Build",
        routes: [
          {
            title: "Kusama Docs",
            link: ""
          },
          {
            title: "Learn Substrate",
            link: ""
          }
        ]
      },
      {
        title: "Validate",
        routes: [
          {
            title: "Start Validating",
            link: ""
          },
          {
            title: "Technical Updates",
            link: ""
          }
        ]
      },
      {
        title: "Join",
        routes: [
          {
            title: "Ambassador Program",
            link: ""
          },
          {
            title: "Nominate a Validator",
            link: ""
          }
        ]
      }
    ]);
    return {
      cards
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../../scss/colors.scss";
.portfolio {
  background-color: $background-color-black;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  position: relative;
  width: 100%;
  .row {
    width: 100%;
  }
}
.take-flight {
  width: 100%;
}
</style>
