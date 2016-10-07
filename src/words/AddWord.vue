<template lang="html">
<div class="jumbotron">
  <form v-on:submit="handleSubmit" v-if="active">
  <h4>Add Words Here!</h4>
    <div class="form-group">
      <input type="text" class="form-control" name="adjective" placeholder="Adjective"
      v-model="newAdjective.text">
    </div>

    <div class="form-group">
      <input type="text" class="form-control" name="noun" placeholder="Noun"
      v-model="newNoun.text">
    </div>

    <button type="submit" class="btn btn-lg btn-block btn-primary">
      Add Word(s)
    </button>
  </form>
</div>
</template>

<script>
export default {
  data() {
    return {
      active: true,
      newAdjective: { id: null, text: null, selected: false },
      newNoun: { id: null, text: null, selected: false }
    };
  },
  methods: {
    handleSubmit(e) {
      e.preventDefault();
      this.$emit('wordAdded', { adjective: this.newAdjective, noun: this.newNoun });
    }
  }
};
</script>

<style lang="css" scoped>
form {
  padding: 5px;
  background: #ECF0F1;
  border-radius: 2px;
}
</style>
