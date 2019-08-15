<template>
  <v-app >
      <v-toolbar app dark class="primary">
          <v-toolbar-title v-text="'Users Cab'"></v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items>
            <v-btn v-for="(item,i) in menuItems" flat :key="`menuitem${i}`" :to="item.route">
                <v-icon left v-html="item.icon" ></v-icon>
                {{item.title}}
            </v-btn>
          </v-toolbar-items>
      </v-toolbar>
  </v-app>
</template>

<script>
export default {
    computed:{
        menuItems(){
            return[
                {
                    icon:  'visibility',
                    title:'About',
                    route: '/about'
                },
               {
                    icon:  'extention',
                    title:'User list',
                    route: '/ulist'
                },
               {
                    icon:  'account_circle',
                    title:'My Account',
                    route: '/profile'
                },
                {
                    icon:  'exit_to_app',
                    title:'LogOut',
                    route: '/logout'
                },
                {
                    icon:  'input',
                    title:'LogIn',
                    route: '/login'
                },
                {
                    icon:  'lock_open',
                    title:'SignUp',
                    route: '/signup'
                }
            ]
        }
    }

}
</script>

<style scoped>

</style>