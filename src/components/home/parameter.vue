<template>
  <v-card>
    <v-tabs v-model="tab">
      <v-tab> Body </v-tab>
      <v-tab> Query String </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item>
        <textarea name="" rows="5" class="tab-text-area"></textarea>
      </v-tab-item>
      <v-tab-item>
        <v-card>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      tab: null,
      items: [
        {tab: 'Body', content: 'Tab body'},
        {tab: 'Params', content: 'Tab params'},
      ],
    };
  },
};
</script>


<style scoped>
.tab-text-area {
  width: 100%;
  outline: none;
  padding: 10px 20px;
}
</style>
