<template lang="html">
<div class="jumbotron col-md-8">
  <div>
    <h2>You {{ adjective.text }} {{ noun.text }}!</h2>
  </div>
</div>
</template>

<script>
export default {
  props: ['adjective', 'noun']
};
</script>

<style lang="css" scoped>
.jumbotron { margin-top: 30px; }
</style>
