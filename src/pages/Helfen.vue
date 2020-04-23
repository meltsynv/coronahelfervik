<template>
  <q-page class="wrapper">
    <Regionalesuche class="q-mb-xl" />
    <Seperator/>
    <BlockCard/>
    <BlockCard/>
    <BlockCard/>
    <BlockCard/>
  </q-page>
</template>

<script>
import Regionalesuche from "components/Regionalesuche";
import BlockCard from "components/BlockCard";
import Seperator from 'components/Seperator';
export default {
  components: {
    Regionalesuche,
    BlockCard,
    Seperator
  }
};
</script>

<style lang="scss">
.wrapper {
  width: 65%;
  margin: 0 auto;
}
</style>