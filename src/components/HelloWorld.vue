<template>
  <div class="hello" @load="onTest">
    <el-form ref="form" :model="form" label-width="auto">
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-checkbox-group v-model="form.type">
            <el-checkbox label="Online activities" name="type"></el-checkbox>
            <!-- <el-checkbox label="Promotion activities" name="type"></el-checkbox> -->
          </el-checkbox-group>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name">
          <el-radio-group v-model="form.resource">
            <el-radio label="Sponsor"></el-radio>
          </el-radio-group>
        </el-form-item>
      </div>
      <div class="test-form-group">
        <el-form-item label="Activity name tes123123123t">
          <el-select
            v-model="form.region"
            placeholder="please select your zone"
          >
            <el-option label="Zone one" value="shanghai"></el-option>
            <el-option label="Zone two" value="beijing"></el-option>
          </el-select>
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
  created() {
    // let node = document.querySelector('#app > div > form > div:nth-child(4) > div > div.el-form-item__label-wrap')
    let node = document.querySelector(".el-form-item__label-wrap");
    console.log("@@@@ node: ", node);
  },
  mounted() {
    let nodes = document.querySelectorAll(".el-form-item__label-wrap");
    console.log("@@@@ node: ", nodes);
    for (let i = 0; i < nodes.length; i++) {
      console.log(nodes[i]);
      console.log(nodes[i].clientWidth);
      console.log(nodes[i].scrollWidth);
      console.log(nodes[i].style);
      // nodes[i].style.marginLeft = '300px'
      // 21
    }

    let contentNodes = document.querySelectorAll(".el-form-item__content");
    console.log(contentNodes);
    for (let i = 0; i < contentNodes.length; i++) {
      console.log(contentNodes[i].style)
      contentNodes[i].style.marginLeft = '300px !important'
      contentNodes[i].style.backgroundColor = 'red';

    }
  },
  updated() {
    console.log("update");
  },
  activated() {
    console.log("activated");
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
    onTest() {
      console.log("load");
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
