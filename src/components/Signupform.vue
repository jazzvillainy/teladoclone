<template>
  <form>
    <div>
        <p style="height:50px">*Required</p>
    </div>

    <div>
      <label>First Name* </label> <input type="text" required v-model="name" />
    </div>

    <div>
      <label>Last Name* </label>
      <input type="text" required v-model="lastName" />
    </div>

    <div>
      <label>Email* </label> <input type="email" required v-model="email" />
    </div>

    <div>
      <label for="">Country*</label>
      <select
        class="select"
        style="padding:15px"
        id="select-country"
        v-model="role"
      >
        <option value="developer">Nigeria</option>
        <!-- <option value="designer">Web Designer</option> -->
      </select>
    </div>

    <div>
      <label for="">ZIP code*</label>
      <input placeholder="    ##### or #####-####" type="text" />
    </div>

    <div>
      <label for="">Sex assigned at birth* </label>
      <select
        class="select"
        style=" display: block"
        name=""
        id=""
      >
        <option value="">Please select</option>
        <option value="">Male</option>
        <option value="">Female</option>
        <option value="">Other</option>
      </select>
    </div>
    <div>
      <label for="">Date Of Birth*</label>
      <p>MM/DD/YYYY</p>
    </div>

    <div>
      <input id="checkbox" type="" placeholder="    MM/DD/YYYY" />
    </div>

    <div class="lastDiv">
      <input style="width: 30px" type="checkbox" />
      <span style="padding: 3px 0px 10px 10px" for=""
        >I received a Teladoc Health code from my employer or insurance
        company.</span
      >
    </div>

    <button class="">Next</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      email: "mario",
      password: "",
      role: "",
    };
  },
};
</script>

<style scoped>
/* .checkbox {
  display: inline;
} */
* {
  /* border: solid; */
}
button {
  background-color: #5b2f91;
  padding: 10px;
  border-radius: 10px;
  border: none;
  color: white;
}
.select {
  border: 1px solid black;
  border-radius: 5px;
  width: 100;
  height: 50px;
}
form {
  display: flex;
  flex-direction: column;
  width: 30%;
  margin: 20% auto;
  margin-top: 0;
  justify-content: space-evenly;
  gap: 20px;
}
label {
  padding: 2px;
  font-weight:bold ;
}
/* @media (max-width: 768px) {
  form {
    width: 90%;
    margin: 20% auto;
    margin-top: 0;
  }
} */
input {
  /* outline: black; */
  border: 1px solid black;
  border-radius: 5px;
  height: 50px;
}
.lastDiv {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  align-content: flex-start;
}
form,
div {
  display: flex;
  flex-direction: column;
}

</style>
