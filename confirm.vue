<template>
  <div id="confirm-form">
    <h1>
      Confirm Your Profile Details
    </h1>
    <body>
    </body>
    <label for="business"> Business:</label>
    <label for="b_name">Name:</label>
    <input type="text" name="b_name" v-model="fields_data.user" >
      <label for="hq_city">HQ City:</label>
        <input type="text" name="hq_city" v-model="fields_data.user" >
    <label for="hq_state">HQ State:</label>
    <input type="text" name="hq_state" v-model="fields_data.pass" >
    <label for="phone_numb">Primary Phone # :</label>
    <input type="text" name="phone_numb" v-model="fields_data.pass" >

<label for="location">Location:</label>
<label for="addr_1">Address Line 1: </label>
  <input type="text" name="addr_1" v-model="fields_data.pass" >
  <label for="addr_2">Address Line 2:</label>
    <input type="text" name="addr_2" v-model="fields_data.pass" >
    <label for="city1"> City: </label>
      <input type="text" name="city1" v-model="fields_data.pass" >
      <label for="state1"> State: </label>
        <input type="text" name="state1" v-model="fields_data.pass" >
        <label for="zip1"> ZIP Code: </label>
          <input type="text" name="zip1" v-model="fields_data.pass" >
          <label for="location_id"> Location Name/ID: </label>
            <input type="text" name="location_id" v-model="fields_data.pass" >
    <input type="submit" name="btn_submit" value="Almost Done" v-on:click="handleClick">
  </div>
</template>

<script>
var CryptoJS = require("crypto-js")
export default {
	name: 'RegistrationForm',
  data: function(){
    return{
      fields_data: {
        bname: this.fields.bname,
        hqc: this.fields.hqc
        hqs: this.fields.hqs
        pp: this.fields.pp
        add1: this.fields.add1
        add2: this.fields.add2
        cit: this.fields.cit
        stat: this.fields.stat
        zip: this.fields.zip
        locid:this.fields.locid
      }
    }
  },
	props: ["fields", "action"],
    methods: {
      handleClick: function(evt){
        this.action(this.fields_data)
      }
    }
}
</script>
<style></style>
