<template>
  <div class="card card-default">
    <div class="card-header">
      <h3 class="card-title">Poc data entry</h3>

      <div class="card-tools">
        <button type="button" class="btn btn-tool" data-card-widget="collapse">
          <i class="fas fa-minus"></i>
        </button>
        <button type="button" class="btn btn-tool" data-card-widget="remove">
          <i class="fas fa-times"></i>
        </button>
      </div>
    </div>
    <!-- /.card-header -->
    <div class="card-body">
      <div class="row">
        <div class="col-md-6">
          <div class="form-group">
            <label>N</label>
            <input class="form-control" style="width: 100%" v-model="n">
            <label>P</label>
            <input class="form-control" style="width: 100%" v-model="p">
            <label>K</label>
            <input class="form-control" style="width: 100%" v-model="k">
          </div>
          <!-- /.form-group -->
          <div class="form-group">
            
            <label>pH</label>
            <input class="form-control" style="width: 100%" v-model="ph">
            <label>Rainfall</label>
            <input class="form-control" style="width: 100%" v-model="rainfall">
          </div>
          <!-- /.form-group -->
        </div>
        <!-- /.col -->
        <div class="col-md-6">
          <div class="form-group">
            <label>Temperature</label>
            <input class="form-control" style="width: 100%" v-model="temperature">
            <label>Soil humidity</label>
            <input class="form-control" style="width: 100%" v-model="humidity">
          </div>
          <!-- /.form-group -->
          <!-- <div class="form-group">
            <label>Disabled Result</label>
            <select class="form-control select2" style="width: 100%">
              <option selected="selected">Alabama</option>
              <option>Alaska</option>
              <option disabled="disabled">California (disabled)</option>
              <option>Delaware</option>
              <option>Tennessee</option>
              <option>Texas</option>
              <option>Washington</option>
            </select>
          </div> -->
          <!-- /.form-group -->
        </div>
        <!-- /.col -->
      </div>
      <!-- /.row -->

      <!-- <h5>Custom Color Variants</h5> -->
      <div class="row">
        <div class="col-12 col-sm-6">
          <!-- <div class="form-group">
            <label>Minimal (.select2-danger)</label>
            <select
              class="form-control select2 select2-danger"
              data-dropdown-css-class="select2-danger"
              style="width: 100%"
            >
              <option selected="selected">Alabama</option>
              <option>Alaska</option>
              <option>California</option>
              <option>Delaware</option>
              <option>Tennessee</option>
              <option>Texas</option>
              <option>Washington</option>
            </select>
          </div> -->
          <!-- /.form-group -->
        </div>
        <!-- /.col -->
        <div class="col-12 col-sm-6">
          <button class="btn btn-primary" @click="submitForm">Submit</button>
        </div>
        <!-- /.col -->
      </div>
      <!-- /.row -->
    </div>
    <!-- /.card-body -->
    <!-- <div class="card-footer">
      Visit
      <a href="https://select2.github.io/">Select2 documentation</a>
      for more examples and information about the plugin.
    </div> -->
  </div>
</template>

<script>
export default { data() {
    return {
      n: null,
      p: null,
      k: null,
      temperature: null,
      humidity: null,
      ph: null,
      rainfall: null
    };
  },
  methods: {
    submitForm() {
      const data = {
        N: Number(this.n),
        P: Number(this.p),
        K: Number(this.k),
        temperature: Number(this.temperature),
        humidity: Number(this.humidity),
        ph: Number(this.ph),
        rainfall: Number(this.rainfall)
      };
      console.log(data);
    }
  }};
</script>

<style>
</style>