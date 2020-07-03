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

.cards_container {
  margin: 0 auto;
  border: 0px solid white;
  align-content: center;
  text-align: center;
}

.card {
  width: 200px;
  height: 200px;
  background-color: #6c5ce7;
  border-radius: 10px;
  display: inline-block;
  margin: 10px 20px 10px 20px;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.2), 0 4px 24px 0 rgba(0, 0, 0, 0.19);
  transform: scale(1);
  animation: pulse 5s infinite;
}

@keyframes pulse {
  0% {
    transform: scale(0.95);
  }

  50% {
    transform: scale(1);
  }

  100% {
    transform: scale(0.95);
  }
}

.flip_card {
  width: 210px;
  height: 200px;
  background-color: #6c5ce7;
  border-radius: 10px;
  display: inline-block;
  margin: 10px 20px 10px 20px;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.2), 0 4px 24px 0 rgba(0, 0, 0, 0.19);
  transform: scale(1);
  animation: pulse 5s infinite;
  perspective: 1000;
  min-height: 120px;
  cursor: pointer;
}

/* This container is needed to position the front and back side */
.flip_card_inside {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Does a horizontal flip when you mouse over */
.flip_card:hover .flip_card_inside {
  transform: rotateY(180deg);
}

/* Positions the front and back side */
.flip_card_front,
.flip_card_back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

.flip_card_back {
  background-color: #ffffff;
  color: #000000;
  transform: rotateY(180deg);
  border-radius: 10px;
}

.card_flip_image {
  padding-top: 40px;
}
</style>
