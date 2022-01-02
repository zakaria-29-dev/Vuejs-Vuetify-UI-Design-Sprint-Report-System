<template> 

      <v-navigation-drawer
        v-model="drawer"
        app
        color="white"
       
        mini-variant
        mini-variant-width="80"
      >
        <v-avatar
          class="d-block text-center mx-auto mt-4"
          color=""
          size="40"
        >
        <v-icon color="#49D9A0" large>fab fa-atlassian</v-icon>
        </v-avatar>

        <v-divider class="mx-3 my-5"></v-divider>
         
       <v-list flat  class="mt-5" >
            <v-list-item-group v-model="selectedItem"  >
              
                <v-list-item v-for="(item, i) in items" :key="i" active-class="border" class=""
                :ripple="false"
                >
                    <v-list-item-icon >    
                        <v-icon v-text="item.icon"></v-icon>
                    </v-list-item-icon>
                    </v-list-item> 
            </v-list-item-group>
        </v-list>
        <div style="position: absolute; bottom: 20px;
        margin-left: auto; margin-right: auto; left:0; right: 0; text-align: center;">
                <v-btn icon :ripple="false">
         <v-badge bordered overlap color="red" dot>
        
        <v-icon>far fa-bell</v-icon>
     
         </v-badge>
          </v-btn><br>
           <v-avatar size="30"  >
          <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"></v-img>
        </v-avatar>

        </div>
      </v-navigation-drawer>

    
</template>

<script>
  export default {
    data: () => ({ 
         selectedItem: 0,
        drawer: null,
        items: [
            {icon: 'fas fa-plus'},
            {icon: 'fas fa-th-large'},
            {icon: 'fas fa-align-center'},
            {icon: 'fab fa-gitter'},
            {icon: 'fas fa-chart-line'},
        ],
     }),
  }
</script>
<style>
.border  {
   margin-left: 12px;
   margin-right: 12px;
    background: #49D9A0 ;
    border-radius: 50%;
    text-decoration: none;
    
}
.v-list-item-group .v-list-item--active {
    color: white !important;
}
</style>