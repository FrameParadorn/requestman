<template>
  <v-row>
    <v-col class="d-flex" cols="2">
      <v-select v-model="itemSelect" :items="items" item-value="GET" solo></v-select>
    </v-col>
    <v-col class="d-flex" cols="8">
      <v-text-field label="http://example.com/params=1&params=2" solo></v-text-field>
    </v-col>
    <v-col class="d-flex" cols="2">
      <div class="text-xs-center">
        <v-btn elevation="2" large> Send </v-btn>
      </div>
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
