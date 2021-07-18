<template>
<!-- <Navigation /> -->
  <div class="container">
    <div class="row">
      <div class="">
        <form>
        <h1>Create Currency</h1>
        <div class="col">
          <label for="name" class="form-label"
            >Name</label>
          <input type="text" class="form-control" v-model="name" />
        </div>
        <div class="col mb-2">
          <label for="value" class="form-label">Value</label>
          <input type="text" class="form-control" v-model="value" />
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>

      <p> Name: {{ name}}</p>
      <p> Value: {{ value}}</p>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      name: '',
      value: '',
    };
  },
  name: 'CreateCurrencies',
}
</script>
