<script>
export default {
  name: 'App',
  data() {

    return {
      name: 'Email List:',
      emailList: [],
    };
  },
  methods: {

  },
  mounted() {
    axios
      .get('https://flynn.boolean.careers/exercises/api/random/mail')
      .then((response) => {
        console.log(response.data.response);
      })

    for (let i = 0; i < 10; i++) {
      axios
        .get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          console.log(response.data.response);
        })
    }
  }
};
</script>

<template>
  <div class="container mt-5">
    <div class="card p-3 w-75 m-auto">
      <div class="d-flex justify-content-around align-items-center">
        <h1 class="text-center">{{ name }}</h1>
      </div>
      <div class="d-flex justify-content-center ">
        <ul class="list-group fs-3">
          <li class="list-group-item d-flex justify-content-between" v-for="(email, index) in emailList" :key="index">
            {{ email }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template >

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background-color: #ededed;
}
</style>
