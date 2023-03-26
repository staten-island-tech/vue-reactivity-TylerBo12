<script>
import { ref } from "vue";
import CssVariables from "./CssVariables.vue";
export default {
  components: { CssVariables },
  data() {
    return {
      animalArray: [
        "Aardvark",
        "Albatross",
        "Alligator",
        "Alpaca",
        "Ant",
        "Anteater",
        "Antelope",
        "Ape",
        "Armadillo",
        "Donkey",
        "Baboon",
        "Badger",
        "Barracuda",
        "Bat",
        "Bear",
        "Beaver",
        "Bee",
        "Bison",
        "Boar",
        "Buffalo",
        "Butterfly",
        "Camel",
        "Capybara",
        "Caribou",
        "Cassowary",
        "Cat",
        "Caterpillar",
        "Cattle",
        "Chamois",
        "Cheetah",
        "Chicken",
        "Chimpanzee",
        "Chinchilla",
        "Chough",
        "Clam",
        "Cobra",
        "Cockroach",
        "Cod",
        "Cormorant",
        "Coyote",
        "Crab",
        "Crane",
        "Crocodile",
        "Crow",
        "Curlew",
        "Deer",
        "Dinosaur",
        "Dog",
        "Dogfish",
        "Dolphin",
        "Dotterel",
        "Dove",
        "Dragonfly",
        "Duck",
        "Dugong",
        "Dunlin",
        "Eagle",
        "Echidna",
        "Eel",
        "Eland",
        "Elephant",
        "Elk",
        "Emu",
        "Falcon",
        "Ferret",
        "Finch",
        "Fish",
        "Flamingo",
        "Fly",
        "Fox",
        "Frog",
        "Gaur",
        "Gazelle",
        "Gerbil",
        "Giraffe",
        "Gnat",
        "Gnu",
        "Goat",
        "Goldfinch",
        "Goldfish",
        "Goose",
        "Gorilla",
        "Goshawk",
        "Grasshopper",
        "Grouse",
        "Guanaco",
        "Gull",
        "Hamster",
        "Hare",
        "Hawk",
        "Hedgehog",
        "Heron",
        "Herring",
        "Hippopotamus",
        "Hornet",
        "Horse",
        "Human",
        "Hummingbird",
        "Hyena",
        "Ibex",
        "Ibis",
        "Jackal",
        "Jaguar",
        "Jay",
        "Jellyfish",
        "Kangaroo",
        "Kingfisher",
        "Koala",
        "Kookabura",
        "Kouprey",
        "Kudu",
        "Lapwing",
        "Lark",
        "Lemur",
        "Leopard",
        "Lion",
        "Llama",
        "Lobster",
        "Locust",
        "Loris",
        "Louse",
        "Lyrebird",
        "Magpie",
        "Mallard",
        "Manatee",
        "Mandrill",
        "Mantis",
        "Marten",
        "Meerkat",
        "Mink",
        "Mole",
        "Mongoose",
        "Monkey",
        "Moose",
        "Mosquito",
        "Mouse",
        "Mule",
        "Narwhal",
        "Newt",
        "Nightingale",
        "Octopus",
        "Okapi",
        "Opossum",
        "Oryx",
        "Ostrich",
        "Otter",
        "Owl",
        "Oyster",
        "Panther",
        "Parrot",
        "Partridge",
        "Peafowl",
        "Pelican",
        "Penguin",
        "Pheasant",
        "Pig",
        "Pigeon",
        "Pony",
        "Porcupine",
        "Porpoise",
        "Quail",
        "Quelea",
        "Quetzal",
        "Rabbit",
        "Raccoon",
        "Rail",
        "Ram",
        "Rat",
        "Raven",
        "Red deer",
        "Red panda",
        "Reindeer",
        "Rhinoceros",
        "Rook",
        "Salamander",
        "Salmon",
        "Sand Dollar",
        "Sandpiper",
        "Sardine",
        "Scorpion",
        "Seahorse",
        "Seal",
        "Shark",
        "Sheep",
        "Shrew",
        "Skunk",
        "Snail",
        "Snake",
        "Sparrow",
        "Spider",
        "Spoonbill",
        "Squid",
        "Squirrel",
        "Starling",
        "Stingray",
        "Stinkbug",
        "Stork",
        "Swallow",
        "Swan",
        "Tapir",
        "Tarsier",
        "Termite",
        "Tiger",
        "Toad",
        "Trout",
        "Turkey",
        "Turtle",
        "Viper",
        "Vulture",
        "Wallaby",
        "Walrus",
        "Wasp",
        "Weasel",
        "Whale",
        "Wildcat",
        "Wolf",
        "Wolverine",
        "Wombat",
        "Woodcock",
        "Woodpecker",
        "Worm",
        "Wren",
        "Yak",
        "Zebra",
      ],
      cart: [],
    };
  },
  methods: {
    push: function (item) {
      this.cart.push(item);
      console.log(this.cart);
    },
    displayCart: function () {
      this.cart.forEach((animal) => {
        console.log(animal);
      });
    },
  },
};
</script>

<template>
  <h1>Adoption Shelter</h1>
  <div>
    <button class="shoppingCartBtn" @click="displayCart()">
      <img
        class="shoppingCartBtn"
        src="https://www.models-resource.com/resources/big_icons/49/48807.png?updated=1666220257"
        alt="Img of Nintedo E shop bag as a shopping cart"
      />
    </button>
    <sub class="cartDisplay" v-for="items in cart" :key="items">{{
      items
    }}</sub>
  </div>
  <!-- --------------------------- -->
  <div id="container">
    <div v-for="animals in animalArray" :key="animals" class="child">
      <span class="animals">{{ animals }} </span>
      <button @click="push(animals)">Add to Cart</button>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-size: 10rem;
}
.shoppingCartBtn {
  width: 20rem;
  height: 20rem;
}

.cartDisplay {
  display: flex;
  flex-direction: row;
  font-size: 5rem;
}

#container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  /* --------------------------- */
  width: 150rem;
}

.child {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  /* --------------------------- */
  margin-right: 10rem;
  margin-top: 2rem;
  width: 32rem;
  border-radius: 1rem;
  background-color: var(--siteBacco);
}

.animals {
  display: flex;
  justify-content: center;
  /* --------------------------- */

  font-size: 5rem;
  margin: 2rem;
  width: 30rem;
  border-radius: 1rem;
  /* --------------------------- */
  border: solid var(--cardBorder) 0.5rem;
  background-color: var(--cardColor);
  color: black;
}
button {
  font-size: 2rem;
}
</style>
