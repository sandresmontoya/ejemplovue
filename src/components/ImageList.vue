<template>
  <v-container>
    <v-row>
      <v-col v-for="item in items.hits" v-bind:key="item.id" sm="4" cols="12">
        <v-card>
          <img :src="item.previewURL" alt="">
        </v-card >
      </v-col>
    </v-row>
  </v-container>
</template>


<script>
export default {
  name: "ImageList",
  props: ["items"],
};
</script>