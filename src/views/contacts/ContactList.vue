<template>
    <v-container>
        <v-btn
            bottom color="pink" dark  fab fixed right
            @click="dialog = !dialog"
        >
      <v-icon>mdi-plus</v-icon>
    </v-btn>

  <v-dialog
      v-model="dialog"
      width="800px"
    >
    <ContactForm @cancel="dialog=false" @save="dialog=false" @more="dialog=false" ></ContactForm>
    </v-dialog>

</v-container>
  
</template>

<script>
import ContactForm from './ContactForm'
export default {
    name:"ContactList",
    components:{
        ContactForm
    },
    props:[],
    data:()=>({
                dialog:false
                })
}
</script>

<style>

</style>