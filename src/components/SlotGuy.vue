<template lang="pug">
  .slot-guy
    h4 i m slot guy
    slot
    slot(name="boom")
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class SlotGuy extends Vue {

}
</script>