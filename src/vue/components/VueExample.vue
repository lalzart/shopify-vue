<template>
  <div>
    <h1>Vue Component</h1>
    <p>Shopify Prop: {{ externalProp }}</p>
    <p>Store Value: {{ value }}</p>
    <p>handle: {{ test123.handle }}</p>
  <v-btn>lance</v-btn>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  props:[ "externalProp", "test"],
  data() {
    return {
      test123: JSON.parse(this.test)
    }
  },
  computed: {
    ...mapGetters("example", ["value"])
  }
};
</script>
