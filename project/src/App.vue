<template>
  <div>
    <h1>Cool facts about outer space.</h1>
    <button @click.prevent="getNewFact">Generate a fact</button>
    <div><fact-card :fact="fact" /></div>
    <div class="grow">
       <img src="./../public/dipper.svg" />
    </div>
   
  </div>
</template>

<script>
import { ref } from "vue";
import factCard from "./components/factCard.vue";
export default {
  name: "App",
  components: {
    factCard,
  },
  setup() {
    let fact = ref("");
    const facts = [
      "The Milky Way galaxy is 105,700 light-years wide.",
      "Footprints left on the Moon won’t disappear as there is no wind.",
      "There is no sound in space because molecules are too far apart to transmit sound.",
      "To escape Earth’s gravity, a spacecraft must travel more than 25,008 mph, or near Mach 33.",
      "Pizza Hut Once Delivered Space Pizza to the ISS",
      "When you are on Mars, the sunset looks like it’s blue.",
      "The International Space Station (ISS) is the size of a football field.",
      "Neutron stars can spin at a rate of 600 rotations per second",
      "There is an uncountable number of stars in the known universe",
      "The Apollo astronauts' footprints on the moon will probably stay there for at least 100 million years",
      "99 percent of our solar system's mass is the sun",
      "If two pieces of the same type of metal touch in space, they will bond and be permanently stuck together",
      "If two pieces of the same type of metal touch in space, they will bond and be permanently stuck together",
      "If a star passes too close to a black hole, it can be torn apart.",
      "The hottest planet in our solar system is Venus.",
      "Our solar system is 4.57 billion years old",
      "The highest mountain discovered is the Olympus Mons, which is located on Mars",
      "The Whirlpool Galaxy (M51) was the first celestial object identified as being spiral",
      "The Sun weighs about 330,000 times more than Earth",
      "Pluto is smaller than the United States",
      "According to mathematics, white holes are possible, although as of yet we have found none",
      "There are more stars in space than there are grains of sand in the world",
      "We know more about Mars and our Moon than we do about our oceans",
      "Only 5% of the universe is visible from Earth",
      "There are approximately 100 thousand million stars in the Milky Way.",
      "The first ever black hole photographed is 3 million times the size of Earth",
      "On Venus, it snows metal and rains sulfuric acid",
      "Coca-Cola was the first commercial soft drink that was ever consumed in space",
      "Astronauts can grow approximately two inches (5 cm) in height when in space",
      "The center of the Milky Way smells like rum & tastes like raspberries",
    ];
    function getNewFact() {
      fact.value = facts[Math.floor(Math.random() * facts.length)];
    }

    return {
      fact,
      getNewFact,
    };
  },
};
</script>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif,
    "Times New Roman", Times, serif, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #b8bef0de;
  margin-top: 60px;
}
html {
  background: url(../public/background.jpg) no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}
button {
  width: 25%;
  height: 200%;
  font-size: 19px;
  font-family: 'Leckerli One', cursive;
  text-align: center;
  background-color: rgb(233, 214, 235);
  color: rgb(79, 79, 79);
  border-radius: 40px;
  border-color: white;
}
button:hover {
  cursor: pointer;
}
.grow {
  padding: 50px;
  transition: transform .5s;
  width: 200px;
  height: 200px;
  margin: 0 auto;
}

.grow:hover {
  -ms-transform: scale(1.25); /* IE 9 */
  -webkit-transform: scale(1.25); /* Safari 3-8 */
  transform: scale(1.25); 
}
</style>
