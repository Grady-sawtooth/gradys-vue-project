<template>
  <div class="my-5 card text-center">
    <h2 class="card-header">Counter Example Test2</h2>
    <div class="card-body">
      <div class="row my-4">
        <div class="col-sm-6 col-lg-3 my-2">
          <button @click="add" class="btn btn-primary">Add to count</button>
        </div>
        <div class="col-sm-6 col-lg-3 my-2">
          <button @click="subtract" class="btn btn-primary">Subtract to count</button>
        </div>
        <div class="col-sm-6 col-lg-3 my-2">
          <div class="input-group">
            <input type="number" class="form-control" v-model="amount" />
            <button
              @click="addAmount(amount)"
              class="btn btn-primary"
              type="button"
              id="button-addon2"
            >
              Add {{ amount }} to count
            </button>
          </div>
        </div>
        <div class="col-sm-6 col-lg-3 my-2">
          <button @click="count = 0" class="btn btn-secondary">Reset count</button>
        </div>
        <!-- multiplaction Button -->
        <div class="col-sm-12 my-2">
          <div class="input-group">
            <input type="number" class="form-control" v-model="y" />
            <input type="number" class="form-control" v-model="x" />
            <button @click="multiply" class="btn btn-primary" type="button" id="button-addon2">
              Multiply
            </button>
            <button
              @click="(x = 0), (y = 0), (z = 0)"
              class="btn btn-secondary"
              type="button"
              id="button-addon2"
            >
              reset
            </button>
          </div>
          <button @click="addAmount(z)" class="btn btn-primary" type="button" id="button-addon2">
            add to count
          </button>
          <div v-if="z != 0">{{ z }}</div>
        </div>
      </div>
    </div>
    <h1 class="card-footer text-body-secondary m-0">Count: {{ count }}</h1>
  </div>
  <div class="card" style="width: 18rem">
    <img src="..." class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">Card title</h5>
      <p class="card-text">
        Some quick example text to build on the card title and make up the bulk of the card's
        content.
      </p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
      add {{ price }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      amount: 0,
      price: ' $10.99',
      x: 0,
      y: 0,
      z: 0
    }
  },
  methods: {
    add() {
      this.count++
    },
    subtract() {
      this.count--
    },
    addAmount(g) {
      this.count = this.count + g
    },
    multiply() {
      this.z = this.x * this.y
    }
  }
}
</script>

<style scss scoped></style>
