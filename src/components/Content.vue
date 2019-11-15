<template>
      <v-content>
      <v-container
        class="fill-height"
        fluid
      >
      <Contact></Contact>
      </v-container>
    </v-content>
</template>

<script>
import Contact from '../views/contacts'

export default {
    name:"Content",
    components:{
      Contact
    },
    props:[],
    data:()=>({})
}
</script>

<style>

</style>