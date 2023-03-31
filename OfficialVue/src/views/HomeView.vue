<script>
import CssVariables from "./CssVariables.vue";
import ShoppingCart from "./ShoppingCart.vue";
import CreateCards from "../components/CreateCards.vue";
export default {
  components: { CssVariables, ShoppingCart, CreateCards },
  data() {
    return {
      animalArray: [
        { name: "Aardvark", price: "$75" },
        { name: "Albatross", price: "$35" },
        { name: "Alligator", price: "$47" },
        { name: "Alpaca", price: "$3" },
        { name: "Ant", price: "$31" },
        { name: "Anteater", price: "$16" },
        { name: "Antelope", price: "$85" },
        { name: "Ape", price: "$30" },
        { name: "Armadillo", price: "$19" },
        { name: "Baboon", price: "$24" },
        { name: "Badger", price: "$120" },
        { name: "Barracuda", price: "$8" },
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
        "Donkey",
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
      inCart: true,
    };
  },
  methods: {
    push: function (items) {
      this.cart.push(items);
      console.log(this.cart);
    },
    display: function () {
      this.inCart === !this.inCart;
    },
    removeItems: function (items) {
      this.cart = this.cart.filter((t) => t !== items);
      console.log(items);
    },
  },
};
</script>

<template>
  <div id="parent">
    <sub id="shoppingCart">
      <button class="shoppingCartBtn" @click="display()">
        <img
          class="shoppingCartBtn"
          src="https://www.models-resource.com/resources/big_icons/49/48807.png?updated=1666220257"
          alt="Img of Nintedo E shop bag as a shopping cart"
        />
      </button>
    </sub>
    <sub class="cartDisplay" v-for="items in cart" :key="items"
      ><span v-if="inCart === true"
        ><button class="removeItems" @click="removeItems(items)">
          Remove Item</button
        >{{ items.name }} {{ items.price }}</span
      ></sub
    >
    <!-- --------------------------- -->

    <!-- We can use  @click wit an if statement with JS to make the shopping cart work :D-->
    <div id="container">
      <sub v-for="animals in animalArray" :key="animals" class="child">
        <span class="animals">{{ animals.name }} {{ animals.price }}</span>
        <button @click="push(animals)">Add to Cart</button>
      </sub>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-size: 10rem;
}

#shoppingCart {
  margin-right: 30rem;
}

.shoppingCartBtn {
  width: 20rem;
  height: 20rem;
  margin-right: 10rem;
}

.cartDisplay {
  display: flex;
  flex-direction: row;
  /* --------------------------- */
  font-size: 4rem;
  margin-right: 1rem;
  /*  --------------------------- */
  color: black;
}

.removeItems {
  width: 10rem;
  margin-right: 1rem;
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
