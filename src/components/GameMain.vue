<template>
  <div class="wrapper">
    <div class="cards_container">
      <!--go through and render list of cards from array-->

      <div v-for="(card, index) in cards" :key="card.id" class="flip_card">
        <div class="card_index_imagepath">{{ index }}. {{ card.image }}</div>

        <div class="flip_card_inside">
          <div class="flip_card_front"></div>
          <div class="flip_card_back">
            <img :src="card.image" class="card_flip_image" />
            <!--<img v-for="(card, index) in cards" :src="card.img"/>-->
            <!--<img src="assets/emoji_man_mediumdarktone.png">-->
            <!--<li v-for="(card, index) in cards">{{card.img}}</li>-->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      cards: [
        {
          id: 1,
          name: "Person Dark Tone",
          image: "./assets/emoji_person_darktone.png"
        },

        {
          id: 2,
          name: "Woman Medium Tone",
          image: "assets/emoji_woman_mediumdarktone.png"
        },

        {
          id: 3,
          name: "Man Medium Tone",
          image: "assets/emoji_man_mediumdarktone.png"
        },

        {
          id: 4,
          name: "Bearded Medium Tone",
          image: "assets/emoji_manbeard_mediumdarktone.png"
        },

        {
          id: 5,
          name: "Man Medium Tone",
          image: "assets/emoji_man_mediumdarktone.png"
        },

        {
          id: 6,
          name: "Bearded Medium Tone",
          image: "assets/emoji_manbeard_mediumdarktone.png"
        },

        {
          id: 7,
          name: "Person Dark Tone",
          image: "assets/emoji_person_darktone.png"
        },

        {
          id: 8,
          name: "Woman Medium Tone",
          image: "assets/emoji_woman_mediumdarktone.png"
        }
      ]
    };
  }
};
</script>

<style>
.card_index_imagepath {
  display: none;
}
</style>
