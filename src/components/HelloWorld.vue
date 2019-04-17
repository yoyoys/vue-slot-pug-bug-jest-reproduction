<template lang="pug">
  .hello
    h3 {{ msg }}
    SlotGuy
      h4 slot in slot guy
      template(#boom)
        h5 boom slot in slot guy
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import SlotGuy from './SlotGuy.vue';
@Component({
  components: { SlotGuy },
})
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
