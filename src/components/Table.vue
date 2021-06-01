<template>
  <div>
    <b-table striped hover :items="items"></b-table>
    <b-pagination
        align="right"
        v-model="currentPage"
        :total-rows="rows"
        :per-page="perPage"
        aria-controls="my-table"
    ></b-pagination>
  </div>
</template>

<script>
export default {
  name: "Table",
  // props: {
  //   items: {
  //     type: [],
  //     default: []
  //   }
  // },
  data() {
    return {
      items: [
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' }
      ],
      perPage: 3,
      currentPage: 2
    }
  },
  computed: {
    rows() {
      return this.items.length
    }
  }
}
</script>

<style scoped>

</style>