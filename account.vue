<template>
  <div id="registration-form">
    <h1>
      Soiree
    </h1>
    <body>
      You've been invited to manage your Soiree accout!
     Complete your registration below to get started!
    </body>
    <label for="first_name">First Name</label>
    <input type="text" name="first_name" v-model="fields_data.user" >
      <label for="last_name">Last Name</label>
        <input type="text" name="last_name" v-model="fields_data.user" >
    <label for="business_name">Business Name</label>
    <input type="text" name="business_name" v-model="fields_data.pass" >
    <label for="location_name">Location Name</label>
    <input type="text" name="location_name" v-model="fields_data.pass" >

<label for="email_address">Email</label>
  <input type="text" name="email_address" v-model="fields_data.pass" >
  <label for="pass_word">Password</label>
    <input type="text" name="pass_word" v-model="fields_data.pass" >
    <input type="submit" name="btn_submit" value="Register Now!" v-on:click="handleClick">
  </div>
</template>

<script>
var CryptoJS = require("crypto-js");
export default {
	name: 'RegistrationForm',
  data: function(){
    return{
      fields_data: {
        fname: this.fields.fname,
        lname: this.fields.lname
        bname: this.fields.bname
        locname: this.fields.locname
        email: this.fields.email
        pass: this.fields.pass
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
