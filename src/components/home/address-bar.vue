<template>
  <v-row>
    <v-col class="d-flex" cols="2">
      <v-select v-model="itemSelect" :items="items" item-value="GET" solo></v-select>
    </v-col>
    <v-col class="d-flex" cols="9">
      <v-text-field label="http://example.com" solo></v-text-field>
    </v-col>
    <v-col class="d-flex" cols="1">
        <v-btn elevation="2" large block> Send </v-btn>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => {
    return {
      itemSelect: 'GET',
      items: ['GET', 'POST', 'PUT', 'PATCH', 'DELETE'],
    };
  },
};
</script>
