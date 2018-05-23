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

