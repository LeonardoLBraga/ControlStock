<template>
    <div>
      <h1>{{ title }}</h1>
      <!-- <template> -->
      <v-card v-for="item in items" :key="item.id"
        class="mx-auto"
        max-width="344"
        outlined
      >
        <v-list-item three-line>
          <v-list-item-content>
            <div class="text-overline mb-4">
              Item name 
            </div>
            <v-list-item-title class="text-h5 mb-1">
              Coca-Cola {{ item.nameItem }}
            </v-list-item-title>
            <v-list-item-subtitle>2L {{ item.desc }}</v-list-item-subtitle>
          </v-list-item-content>

          <v-list-item-avatar
            tile
            size="80"
            color="grey"
          ></v-list-item-avatar>
        </v-list-item>

        <v-card-actions>
          <v-btn
            outlined
            rounded
            text
          >
            Edit
          </v-btn>
          <v-btn
            outlined
            rounded
            text
          >
            Delete
          </v-btn>
        </v-card-actions>
      </v-card>
    <!-- </template> -->
    </div>
</template>
  
  <script>
  
  export default {
    data: function() {
      return {
        // items: [{
        //   id: String,
        //   nameItem: String,
        //   desc: String
        // }],
      }
    },
    name: 'ListaItens', 
    props: {
        title: String,
    },
    created() {
      // var self = this;
      //   axios.get('/meals')
      //       .then(function (response) {
      //       self.meal_choices = response.data;
      //       console.log(response.data);
      //     })
      //     .catch(function (error) {
      //       console.log(error);
      //     });
      const items = [{ id: '1', nameItem: "coca", desc: "2l" }, { id: '2', nameItem: "coca2", desc: "3l" }]
      console.log(items)
    }
  }
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
  h1 {
    padding-bottom: 20px;
  }
  </style>
  