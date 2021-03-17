


<template>
  <div>


    <v-toolbar dense>

      <v-app-bar-nav-icon class="grey--text" @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>SQS Product</v-toolbar-title>

      
     <!-- <v-app-bar class="primary"
     
      >
        <v-list-item v-for="item in items" :key="item.title" router :to="item.route"
        >
          <v-list-item-icon> 
            <v-icon class="white--text">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title class="white--text">{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      
      </v-app-bar>  -->

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <v-btn icon>
          
        <v-icon>mdi-export</v-icon>
       </v-btn>

    </v-toolbar>


    <v-navigation-drawer class="primary white--text" app v-model="drawer" clipped style=""
    >
  
  <!-- <p class="primary">Home</p> -->


     <v-list
        dense
        nav
      >
        <v-list-item v-for="item in items" :key="item.title" router :to="item.route"
        >
          <v-list-item-icon> 
            <v-icon class="white--text">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title class="white--text">{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      
      </v-list> 

    </v-navigation-drawer>
 


  </div>
</template>

<style scoped>
/* .v-toolbar__content {
    background: #fbfbfb;
} */
/* nav.primary.white--text.v-navigation-drawer.v-navigation-drawer--fixed.v-navigation-drawer--open.theme--light {
    margin-top: 49px;
} */

</style>

<script>
  export default {
    data () {
      return {
        drawer:false,
        items: [
          { icon: 'mdi-view-dashboard', title: 'Dashboard',  route: '/' },
          { icon: 'mdi-file' ,title: 'About',  to: '/about', route: '/about' },
          { icon: 'mdi-file',title: 'Inspire',  to: '/inspire', route: '/inspire' },
          { icon: 'mdi-account-box', title: 'Account',  route: '/' },
          { icon: 'mdi-gavel', title: 'Admin',  route: '/'},

        ],
        right: null,
      }
    }
  }
</script>