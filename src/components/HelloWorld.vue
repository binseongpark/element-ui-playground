<template>
  <div class="hello">
    <el-form ref="form" :model="form" label-width="auto">
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name 123123123123213">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
      </div>
    </el-form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      form: {
        name: "",
        region: "",
        date1: "",
        date2: "",
        delivery: false,
        type: [],
        resource: "",
        desc: "",
      },
    };
  },
  methods: {
    onSubmit() {
      console.log("submit!");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.hello {
  width: 500px;
  margin: 0 auto;
}
</style>
