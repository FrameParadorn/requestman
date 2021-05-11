<template>
  <v-card>
    <v-tabs v-model="tab">
      <v-tab> Body </v-tab>
      <v-tab> Query String </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item>
        <prism-editor
          class="body-editor"
          v-model="code"
          :highlight="highlighter"
          line-numbers
          insertSpaces
          :tabSize="4"
        ></prism-editor>
      </v-tab-item>
      <v-tab-item>
        <v-card>
          <TableInput />
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
import { PrismEditor } from "vue-prism-editor";
import "vue-prism-editor/dist/prismeditor.min.css";
import { highlight, languages } from "prismjs/components/prism-core";
import "prismjs/components/prism-clike";
import "prismjs/components/prism-javascript";
import "prismjs/themes/prism-tomorrow.css";
import TableInput from "@/components/table/table-input.vue";

export default {
  components: {
    PrismEditor,
    TableInput,
  },
  data() {
    return {
      code: '{}',
      tab: null,
      items: [
        { tab: "Body", content: "Tab body" },
        { tab: "Params", content: "Tab params" },
      ],
    };
  },
  methods: {
    highlighter(code) {
      return highlight(code, languages.js);
    },
  },
};
</script>

<style scoped>
.tab-text-area {
  width: 100%;
  outline: none;
  padding: 10px 20px;
}

.body-editor {
    background: white;
    color: #ccc;
    font-family: Fira code, Fira Mono, Consolas, Menlo, Courier, monospace;
    font-size: 14px;
    line-height: 1.5;
    padding: 5px;
  }

  .prism-editor__textarea:focus {
    outline: none;
  }

</style>
