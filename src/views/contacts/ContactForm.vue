<template>
   <v-card>
        <v-card-title class="green darken-1">
          Create contact
        </v-card-title>
        <v-container>
          <v-row class="mx-2">
            <v-col cols="12" class="align-center justify-space-between">
              <v-row align="center" class="mr-0">
                <v-avatar size="40px" class="mx-3">
                  <img src="//ssl.gstatic.com/s2/oz/images/sge/grey_silhouette.png" alt="" >
                </v-avatar>
                <v-text-field
                  placeholder="Name"
                />
              </v-row>
            </v-col>
            <v-col cols="6">
              <v-text-field  placeholder="Company">
                    <v-icon slot="prepend" >mdi-domain</v-icon>
              </v-text-field>
            </v-col>
            <v-col cols="6">
              <v-text-field placeholder="Job title" />
            </v-col>
            <v-col cols="12">
              <v-text-field  placeholder="Email">
                                      <v-icon slot="prepend" >mdi-email</v-icon>
              </v-text-field>
            </v-col>
            <v-col cols="12">
              <v-text-field type="tel"  placeholder="(000) 000 - 0000">
                      <v-icon slot="prepend" >mdi-phone</v-icon>

              </v-text-field>
            </v-col>
            <v-col cols="12">
              <v-text-field    placeholder="Notes">
                  <v-icon slot="prepend" >mdi-text</v-icon>

              </v-text-field>
            </v-col>
          </v-row>
        </v-container>
        <v-card-actions>
          <v-btn text color="primary" @click="$emit('more')" >More</v-btn>
          <v-spacer />
          <v-btn text color="primary" @click="$emit('cancel')">Cancel</v-btn>
          <v-btn text @click="$emit('save')">Save</v-btn>
        </v-card-actions>
      </v-card>
</template>

<script>
export default {
    name:"ContactForm",
    props:[],
    data:()=>({})
}
</script>

<style>

</style>