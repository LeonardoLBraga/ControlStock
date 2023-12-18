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
              {{ item.nameItem }}
            </v-list-item-title>
            <v-list-item-subtitle>
              {{ item.desc }}
            </v-list-item-subtitle>
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
    mounted() {
      // this.loadItemsList();
    },
    data: function() {
      return {
        items: [
         {
            id: '1',
            nameItem: 'Coca-Cola',
            desc: 'Tem 2 litros'
         },
         {
            id: '2',
            nameItem: 'Guarana',
            desc: 'Tem 2 litros'
         }
        ]
      }
    },
    name: 'ListaItens', 
    props: {
        title: String,
    },
    // created() {
    //   
    // },
    methods: {
      // loadItemsList() {
        // axios.get('/api/projects')
        //   .then(response => {
        //       this.projects = response.data;
        //       return response
        //   })
        //   .catch(error => {
        //     return error
        //   });
      // }
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
  