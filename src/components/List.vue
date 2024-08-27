<template>
  <div class="text-center my-4">{{ list }}</div>
  <ul>
    <li v-for="item in list" :key="item">{{ item }}</li>
  </ul>
  <div class="input-group">
    <input type="text" class="form-control" v-model="addToList" />
    <button @click="addToArray(addToList)" class="btn btn-primary" type="button" id="button-addon2">
      Add
    </button>
  </div>
  <div class="input-group">
    <input type="text" class="form-control" v-model="deleteFromList" />
    <button
      @click="deleteFromArray(deleteFromList)"
      class="btn btn-primary"
      type="button"
      id="button-addon2"
    >
      Delete
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: ['Wapiti', 'fire'],
      addToList: '',
      deleteFromList: ''
    }
  },
  methods: {
    addToArray(x) {
      this.list.push(x)
      this.addToList = ''
    },
    deleteFromArray(y) {
      this.list = this.list.filter(remove)
      this.deleteFromList = ''

      function remove(word) {
        return word != y
      }
    }
  }
}
</script>

<style scoped></style>
