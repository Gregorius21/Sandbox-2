<template>
  <div class="row">
    <div class="col-md-3">
      <label for="">Input</label>
    </div>
    <div class="col-md-9">
      <input type="text" v-model="val" class="form-control">
    </div>
  </div>
</template>
<script>
export default {
  props: {
    value: { type: String, default: "" },
  },
  computed: {
    val: {
      get() {
        return this.value;
      },
      set(value) {
        this.editValue(value);
      },
    },
  },
  methods: {
    editValue(value) {
      console.log(value);
      this.$emit("get", value);
    },
  },
};
</script>