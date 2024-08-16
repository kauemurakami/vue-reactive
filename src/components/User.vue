<script setup>
  import {ref, reactive} from 'vue'
  //usando ref
  // const name = ref("Kauê murakami")
  // const birthday = ref(0)
  // const age = ref(25)
  // console.log(age.value)
  // age.value = 27

  //usando reactive
  const user = reactive({
    name: "",
    birthday: "",
    age : 0
  })
</script>

<template>
  <div>
    //com ref
    // <form class="form">
    //   <label for="name">Name: </label><br/>
    //   <input type="text" id="name" name="name" v-model="name"><br/>
    //   <label for="birthday">Birthday *01/05/1990: </label><br/>
    //   <input type="text" id="birthday" name="birthday" v-model="birthday"><br/>
    // </form>

    //com reactive
    <form class="form">
      <label for="name">Name: </label><br/>
      <input type="text" id="name" name="name" v-model="user.name"><br/>
      <label for="birthday">Birthday *01/05/1990: </label><br/>
      <input type="text" id="birthday" name="birthday" v-model="user.birthday"><br/>
    </form>
  </div>
  <p style="text-align: center; overflow-wrap: normal;">{{ user.name }} nasceu em {{ user.birthday }}</p>
</template>


<style scoped>
.form {
  margin: 0 auto;
  padding: 5px;
  width: 200px;
  background-color: darkcyan;
}


</style>