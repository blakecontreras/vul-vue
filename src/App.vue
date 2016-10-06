<template lang="html">
  <div id="app">
    <header>
      <nav class="navbar">
        <div class="navbar-header">
          <a href="/" class="navbar-brand">The Vulgaritor</a>
        </div>
      </nav>
    </header>

    <div class="row">
      <div class="col-md-4">
        <h3>Build Your Insult</h3>
        <div class="col-md-6">
          <h3>Adjectives</h3>
            <div v-for="adjective in adjectives"
            >
              {{ adjective.text }}
            </div>
          </div>
        <div class="col-md-6">
          <h3>Nouns</h3>
          <div v-for="noun in nouns"
          >
            {{ noun.text }}
          </div>
        </div>
      </div>
      Phrase goes here
      <div class="col-md-8 pull-right">
        Add Word goes here
      </div>
    </div>

    <footer class="text-center">
      &copy; 2016
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      adjectives: [
        { id: 0,
          text: "pustulent",
          selected: false
        },
        { id: 1,
          text: "cantankerous",
          selected: false
        },
        { id: 2,
          text: "poxy",
          selected: false
        },
        { id: 3,
          text: "indolent",
          selected: false
        },
        { id: 4,
          text: "shiftless",
          selected: false
        },
        { id: 5,
          text: "typescripty",
          selected: false
        },
        { id: 6,
          text: "boorish",
          selected: false
        },
      ],
      nouns: [
        { id: 0,
          text: "dairy farmer",
          selected: false
        },
        { id: 1,
          text: "cow",
          selected: false
        },
        { id: 2,
          text: "pirate",
          selected: false
        },
        { id: 3,
          text: "pig",
          selected: false
        },
        { id: 4,
          text: "jockey",
          selected: false
        },
        { id: 5,
          text: "weasel",
          selected: false
        },
        { id: 6,
          text: "submariner",
          selected: false
        },
      ],
      selectedAdjective: {id: null, text: "...", selected: null},
      selectedNoun: {id: null, text: "...", selected: null},
    };
  },
  methods: {

  },
  components: {

  }
};
</script>

<style lang="css">
</style>
