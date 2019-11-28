<template>
  <div>
    <form id="myForm" action="#" method="get">
      Firstname:
      <input type="text" name="firstname" v-model="firstname" size="20" />
      <br />Lastname:
      <input type="text" name="lastname" v-model="lastname" size="20" />
      <br />
      <br />
      <input type="Submit"  value="默认Submit" />
      <input type="button" @click="formSubmit()" value="Submit" />
    </form>
    <br />
    <div>
      提交表单action：{{result}}
      <br />
    </div>
  </div>
</template>

<script>
export default {
  name: "form-sample",
  data() {
    return {
      firstname: "",
      lastname: "",
      result: ""
    }
  },
  methods: {
    formSubmit() {
      document.getElementById("myForm").submit()
    }
  }
}
</script>

<style lang="scss" scoped>
</style>