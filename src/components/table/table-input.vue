<template>
  <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">Key</th>
          <th class="text-left">Value</th>
          <th>Option</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in inputs" :key="item.name">
          <td>
            <input type="text" class="table-text-input" placeholder="key" />
          </td>
          <td>
            <input type="text" class="table-text-input" placeholder="value" />
          </td>
          <td>
            <v-btn elevation="2" x-small>DEL</v-btn>
          </td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</template>

<script>
export default {
  data() {
    return {
      inputs: [
        {
          key: 'Frozen Yogurt',
          value: 159,
        },
        {
          key: 'Frozen Yogurt',
          value: 159,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.table-text-input {
  height: 40px;
  width: 100%;
  outline: none;
}
</style>
