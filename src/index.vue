<template>
  <v-data-table
    :headers="headers"
    :items="items"
    :itemsPerPage="itemsPerPage"
    :loading="loading"
    hide-default-footer
    show-select>
    <template v-for="(slot, i) in $slots" v-slot:item.[slot]="{ item }">

    </template>

    <!--    <template v-slot:item.clicks="{ item }">-->
    <!--      <span>{{ item.clicks || 0 }}</span>-->
    <!--    </template>-->

    <!--    <template v-slot:item.prices="{ item }">-->
    <!--      {{-->
    <!--        item.prices && item.prices.length > 0-->
    <!--          ? item.prices[0].expire_at_days + ' روز تا انقضا'-->
    <!--          : ' منقضی شده'-->
    <!--      }}-->
    <!--    </template>-->
  </v-data-table>
</template>

<script>
export default {
  name: "index.vue",

  props: {
    items: Array,
    itemsPerPage: Number,
    loading: Boolean,
    headers: Array,
  },

  data: () => ({
    itemsPerPage: 10,
    options: {},
  })
}
</script>

<style scoped>

</style>