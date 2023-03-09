<template>
  <v-container>
    <v-row>
      <span class="mt-4">Wissenschaftliche Kommissionen:&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp</span>

      <v-select style="width:10px; height:10px;" label="Select" :items="['option 1', 'option 2', 'option 3']"
        v-model="wissKomm"></v-select>
      <v-spacer></v-spacer>
    </v-row>
    <v-row class="mt-10">
      <v-table>
        <thead>
          <tr>
            <th class="text-left">
              Titel
            </th>
            <th class="text-left">
              Wissenschaftliche Qualität
            </th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in publications" :key="item.name">
            <td>{{ item.name }}</td>
            <td>
              <form>
                <label class="radio-inline">
                  <input type="radio" name="optradio" checked> A &nbsp
                </label>
                <label class="radio-inline">
                  <input type="radio" name="optradio"> B &nbsp
                </label>
                <label class="radio-inline">
                  <input type="radio" name="optradio"> C &nbsp
                </label>
              </form>
            </td>
          </tr>
        </tbody>
      </v-table>
    </v-row>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      wissKomm: 'option 1',
      //Dynamically generate publications according to wissenschaftliche kommission
    }
  },
  computed: {
    publications() {
      switch (this.wissKomm) {
        case "option 1":
          return [{
            name: 'pub 1',
          },
          {
            name: 'pub 2',
          },
          {
            name: 'pub 3',
          }]
        case "option 2":
          return [{
            name: 'pub 4',
          },
          {
            name: 'pub 5',
          },
          {
            name: 'pub 6',
          },
          {
            name: 'pub 7',
          },
          {
            name: 'pub 8',
          }]
        case "option 3":
          return [{
            name: 'pub 9',
          },
          {
            name: 'pub 10',
          },
          {
            name: 'pub 11',
            
          },
          {
            name: 'pub 12',
          }]
      }
    },
  },
  methods: {
  }
}
</script>
<style></style>




