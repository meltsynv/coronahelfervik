<template>
  <q-input class="regionale-suche-input" placeholder="Regionale Suche">
    <template v-slot:append>
      <q-icon class="room-icon" name="room" />
    </template>
  </q-input>
</template>

<script>
export default {
}
</script>

<style lang="scss">
.room-icon {
  font-size: 44px;
  color: $primary;
}
.regionale-suche-input {
  margin-top: 50px;
  background-color: $inputcolor;
  padding: 15px;
  font-size: 20px;
  color: $secondary;
}
::placeholder {
  font-size: 20px;
  color: $secondary;
}
</style>