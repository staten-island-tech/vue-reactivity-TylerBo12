<script>
import CssVariables from "./CssVariables.vue";
import cartButton from "../components/CartButton.vue";
import cart from "../components/ShoppingCart.vue";
import create from "../components/CreateCards.vue";
export default {
  components: { CssVariables, create, cart, cartButton },
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
        { name: "Bat", price: "$93" },
        { name: "Bear", price: "$103" },
        { name: "Beaver", price: "$128" },
        { name: "Bee", price: "$193" },
        { name: "Bison", price: "$154" },
        { name: "Boar", price: "$71" },
        { name: "Buffalo", price: "$61" },
        { name: "Butterfly", price: "$123" },
        { name: "Camel", price: "$199" },
        { name: "Capybara!", price: "$128" },
        { name: "Caribou", price: "$179" },
        { name: "Cassowary", price: "$113" },
        { name: "Cat", price: "$136" },
        { name: "Catterpillar", price: "$134" },
        { name: "Cattle", price: "$68" },
        { name: "Chamois", price: "$27" },
        { name: "Cheetah", price: "$62" },
        { name: "Chicken", price: "$159" },
        { name: "Chimpanzee", price: "$121" },
        { name: "Chinchilla", price: "$160" },
        { name: "Chough", price: "$172" },
        { name: "Clam", price: "$58" },
        { name: "Cobra", price: "$38" },
        { name: "Cockroach", price: "$71" },
        { name: "Cod", price: "$139" },
        { name: "Cormorant", price: "$27" },
        { name: "Coyote", price: "$48" },
        { name: "Crab", price: "$59" },
        { name: "Crane", price: "$99" },
        { name: "Crocodile", price: "$72" },
        { name: "Crow", price: "$82" },
        { name: "Curlew", price: "$129" },
        { name: "Deer", price: "$66" },
        { name: "Dinosaur", price: "$177" },
        { name: "Dog", price: "$134" },
        { name: "Dogfish", price: "$186" },
        { name: "Dolphin", price: "$39" },
        { name: "Donkey", price: "$108" },
        { name: "Dotterel", price: "$160" },
        { name: "Dove", price: "$149" },
        { name: "Dragonfly", price: "$27" },
        { name: "Duck", price: "$186" },
        { name: "Dugong", price: "$184" },
        { name: "Dunlin", price: "$56" },
        { name: "Eagle", price: "$224" },
        { name: "Knuckels the Echidna :)", price: "" },
        { name: "Eel", price: "$89" },
        { name: "Eland", price: "$118" },
        { name: "Elephant", price: "$80" },
        { name: "Elk", price: "$76" },
        { name: "Emu", price: "$239" },
        { name: "Falcon", price: "$131" },
        { name: "Ferret", price: "$172" },
        { name: "Finch", price: "$270" },
        { name: "Fish", price: "$109" },
        { name: "FLamingo", price: "$149" },
        { name: "Fly", price: "$42" },
        { name: "Fox", price: "$75" },
        { name: "Frog", price: "$230" },
        { name: "Gaur", price: "$159" },
        { name: "Gazelle", price: "$57" },
        { name: "Gerbil", price: "$248" },
        { name: "Giraffe", price: "$40" },
        { name: "Gnat", price: "$103" },
        { name: "Gnu", price: "$68" },
        { name: "Goat", price: "$247" },
        { name: "Goldfinch", price: "$203" },
        { name: "GOldfish", price: "$45" },
        { name: "Goose", price: "$160" },
        { name: "Gorilla", price: "$202" },
        { name: "Goshawk", price: "$209" },
        { name: "Grasshopper", price: "$269" },
        { name: "Grouse", price: "$101" },
        { name: "Guanaco", price: "$54" },
        { name: "SEAgull", price: "$239" },
        { name: "Hampter", price: "$95" },
        { name: "Hare", price: "$179" },
        { name: "Hawk", price: "$33" },
        { name: "Sonic the Hedgehog", price: "" },
        { name: "Heron", price: "$99" },
        { name: "Herring", price: "$43" },
        { name: "Hippopotamus", price: "$223" },
        { name: "Hornet", price: "$97" },
        { name: "Horse", price: "$253" },
        { name: "Human??", price: "Um No" },
        { name: "Hummingbird", price: "$49" },
        { name: "Hyena", price: "$69" },
        { name: "Ibex", price: "$176" },
        { name: "Ibis", price: "$159" },
        { name: "Jackal", price: "$161" },
        { name: "Jaguar", price: "$30" },
        { name: "Jay", price: "$126" },
        { name: "Jellyfish", price: "$62" },
        { name: "Kangaroo", price: "$35" },
        { name: "Kingfisher", price: "$128" },
        { name: "Koala", price: "$27" },
        { name: "Kookabura", price: "$195" },
        { name: "Kouprey", price: "$233" },
        { name: "Kudu", price: "$203" },
        { name: "Lapwing", price: "$79" },
        { name: "Lark", price: "$71" },
        { name: "Lemur", price: "$47" },
        { name: "Leopard", price: "$215" },
        { name: "Lion", price: "$204" },
        { name: "Llama", price: "$64" },
        { name: "Lobster", price: "$171" },
        { name: "Locust", price: "$42" },
        { name: "Loris", price: "$67" },
        { name: "Louse", price: "$16" },
        { name: "Lyrebird", price: "$66" },
        { name: "Magpie", price: "$243" },
        { name: "Mallard", price: "$215" },
        { name: "Manatee", price: "$176" },
        { name: "Mandrill", price: "$74" },
        { name: "Mantis", price: "$81" },
        { name: "Marten", price: "$44" },
        { name: "Meerkat", price: "$32" },
        { name: "Mink", price: "$146" },
        { name: "Mole", price: "$73" },
        { name: "Bagel the Mongoose", price: "RIP :(" },
        { name: "Monkey", price: "$181" },
        { name: "Moose", price: "$274" },
        { name: "Mosquito", price: "$126" },
        { name: "Mouse", price: "$112" },
        { name: "Mule", price: "$40" },
        { name: "Narwhal", price: "$262" },
        { name: "Newt", price: "$202" },
        { name: "Nightingale", price: "$48" },
        { name: "Octopus", price: "$121" },
        { name: "Okapi", price: "$270" },
        { name: "Opossum", price: "$247" },
        { name: "Oryx", price: "$258" },
        { name: "Ostrich", price: "$188" },
        { name: "Otter", price: "$266" },
        { name: "Owl", price: "$177" },
        { name: "Oyster", price: "$76 " },
        { name: "Panther", price: "$288" },
        { name: "Parrot", price: "$284" },
        { name: "Partridge in a pear tree!", price: "Caroling" },
        { name: "Peafowl", price: "$148" },
        { name: "Pelican", price: "$158" },
        { name: "Penguin", price: "$116" },
        { name: "Pheasant", price: "$227" },
        { name: "Pig", price: "$43" },
        { name: "Pigeon", price: "$179" },
        { name: "Pony", price: "$93" },
        { name: "Porcupine", price: "$180" },
        { name: "Porpoise", price: "$75" },
        { name: "Quail", price: "$168" },
        { name: "Quelea", price: "$102" },
        { name: "Quetzal", price: "$249" },
        { name: "Rabbit", price: "$84" },
        { name: "Raccoon", price: "$139" },
        { name: "Rail", price: "$237" },
        { name: "Ram", price: "$147" },
        { name: "Rat", price: "$98" },
        { name: "Raven", price: "$129" },
        { name: "Red deer", price: "$108" },
        { name: "Red panda", price: "$210" },
        { name: "Reindeer", price: "$171" },
        { name: "Rhinoceres", price: "$83" },
        { name: "Rook(Chess?)", price: "$178" },
        { name: "Salamander", price: "$154" },
        { name: "Salmon", price: "$213" },
        { name: "Sand dollar", price: "$184" },
        { name: "Sandpiper", price: "$82" },
        { name: "Sardine", price: "$126" },
        { name: "Scoprian", price: "$178" },
        { name: "Seahorse", price: "$125" },
        { name: "Spheel", price: "$310" },
        { name: "Shark", price: "$44" },
        { name: "Sheep", price: "$273" },
        { name: "Shrew", price: "$238" },
        { name: "Skunk", price: "$83" },
        { name: "Snail", price: "$202" },
        { name: "Snake", price: "$163" },
        { name: "Sparrow", price: "$113" },
        { name: "Spider", price: "$239" },
        { name: "Spoonbill", price: "$170" },
        { name: "Squid", price: "$39" },
        { name: "Squirrel", price: "$43" },
        { name: "Starling", price: "$138" },
        { name: "Stingray", price: "$189" },
        { name: "Stinkbug", price: "$256" },
        { name: "Stork", price: "$37" },
        { name: "Swallow", price: "$144" },
        { name: "Swan", price: "$266" },
        { name: "Tapir", price: "$42" },
        { name: "Tarsier", price: "$100" },
        { name: "Termite", price: "$160" },
        { name: "Tiger", price: "$95" },
        { name: "Toad", price: "$44" },
        { name: "Trout", price: "$285" },
        { name: "Turkey", price: "$59" },
        { name: "Turtle", price: "$141" },
        { name: "Viper", price: "$286" },
        { name: "Vulture", price: "$156" },
        { name: "Wallaby", price: "$66" },
        { name: "Walrus", price: "$173" },
        { name: "Wasp", price: "$151" },
        { name: "Weasel", price: "$267" },
        { name: "Whale", price: "$238" },
        { name: "Wildcat", price: "$157" },
        { name: "Wolf", price: "$57" },
        { name: "Wolverine", price: "$65" },
        { name: "Wombat", price: "$62" },
        { name: "Woodcock???", price: "$86" },
        { name: "Woodpecker", price: "$109" },
        { name: "Worm", price: "$31" },
        { name: "Wren", price: "$211" },
        { name: "Yak", price: "$135" },
        { name: "Zebra", price: "$54" },
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
      this.inCart = !this.inCart;
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
    <sub>
      <cartButton :cart="cart.length" @click="display()" />
    </sub>
    <sub v-if="inCart === true">
      <cart
        v-for="items in cart"
        :key="items.id"
        :name="items.name"
        :price="items.price"
        @click="removeItems(items)"
      />
    </sub>
    <sub v-else></sub>
    <sub id="container">
      <create
        @click="push(animals)"
        v-for="animals in animalArray"
        :key="animals.name"
        :name="animals.name"
        :price="animals.price"
      />
    </sub>
  </div>
</template>

<style scoped>
h1 {
  font-size: 5rem;
  color: aliceblue;
}

#container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  width: 140rem;
}
</style>
