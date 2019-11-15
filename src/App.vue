<template>
  <v-app>
    <Sidebar :items="items" :drawer="drawer" @toggleDrawer="drawer=$event" ></Sidebar>
    <Navbar :drawer="drawer" @toggleDrawer="drawer=!drawer" ></Navbar>
    <Content ></Content>
  </v-app>
</template>

<script>

import Sidebar from './components/Sidebar'
import Navbar from './components/Navbar'
import Content from './components/Content'


export default {
  name:"App",
  components: {
   Sidebar,
   Navbar,
   Content
  },

 data: () => ({
      dialog: false,
      drawer: false,
      items: [
        { icon: 'mdi-contacts', text: 'Contacts' },
        { icon: 'mdi-history', text: 'Frequently contacted' },
        { icon: 'mdi-content-copy', text: 'Duplicates' },
        {
          icon: 'mdi-chevron-up',
          'icon-alt': 'mdi-chevron-down',
          text: 'Labels',
          model: true,
          children: [
            { icon: 'mdi-plus', text: 'Create label' },
          ],
        },
        {
          icon: 'mdi-chevron-up',
          'icon-alt': 'mdi-chevron-down',
          text: 'More',
          model: false,
          children: [
            { text: 'Import' },
            { text: 'Export' },
            { text: 'Print' },
            { text: 'Undo changes' },
            { text: 'Other contacts' },
          ],
        },
        { icon: 'mdi-settings', text: 'Settings' },
        { icon: 'mdi-message', text: 'Send feedback' },
        { icon: 'mdi-help-circle', text: 'Help' },
        { icon: 'mdi-cellphone-link', text: 'App downloads' },
        { icon: 'mdi-keyboard', text: 'Go to the old version' },
      ],
    }),
  methods:{
    test(e){
      console.log("test",e)
    }
  }
}
</script>

<style>

</style>