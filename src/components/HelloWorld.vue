<template>
 MultiSelect value: {{ multiselectValue }}
    <br />
    <br />
    <kendo-multiselect v-model="multiselectValue"
                        :data-source="dataSourceArray"
                        :data-text-field="'text'"
                        :data-value-field="'value'"
                        :placeholder="'Select size...'"
                        :filter="'contains'">
    </kendo-multiselect>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { MultiSelect } from '@progress/kendo-dropdowns-vue-wrapper';
//Vue.use(MultiSelect);

export default defineComponent({
   components: {
        'kendo-multiselect': MultiSelect
    },
    data: function() {
        return {
            multiselectValue: "",
            dataSourceArray: [
                { text: 'Baseball', value: '1' },
                { text: 'Basketball', value: '2' },
                { text: 'Cricket', value: '3' },
                { text: 'Football', value: '4' },
                { text: 'Tennis', value: '5' },
                { text: 'Volleyball', value: '6' }
            ]
        }
    }
});
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
