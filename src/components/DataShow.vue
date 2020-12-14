<template>
  <div class="text-center pt-10">
    <form @submit.prevent="sendEmail">
    <table class="table-fixed mx-auto text-xl md:text-3xl">
      <thead>
        <tr>
          <th class="w-1/4 text-red-600">Confirmed</th>
          <th class="w-1/4 text-blue-600">Active</th>
          <th class="w-1/4 text-green-600">Recovered</th>
          <th class="w-1/4 text-gray-600">Deaths</th>
        </tr>
      </thead>
      <tbody>
        <tr class="pt-10">
          <td class="text-red-600">{{stateConfirmed}}</td>
          <td class="text-blue-600">{{stateActive}}</td>
          <td class="text-green-600">{{stateRecovered}}</td>
          <td class="text-gray-600">{{stateDeaths}}</td>
        </tr>
      </tbody>
    </table>
    <input class="hidden" type="text" name="stateConfirmed" :value="stateConfirmed"/>
    <h1 class="pt-5 text-2xl text-green-600">{{selectedCity}} Confirmed Cases are : {{cityConfirmed}}</h1>
    <i class="block mt-5 text-red-600 text-sm md:text-xl">Send Cases details to your email type your email addres:</i>
    <input type="email" class="w-50 h-30 p-3 mt-5" name="email" v-model="email" placeholder="Enter Your Email here Eg:ratnakarmishraji@gmail.com"/>
    <button type="submit">Send Email</button>
    </form>
  </div>
</template>

<script>

import emailjs from 'emailjs-com';

export default {
  name: "DataShow",
  props: ["stateActive","stateConfirmed","stateRecovered","stateDeaths","selectedCity","cityConfirmed","selectedState"],
  data(){
    return{
      email:"",
    }
  },
 methods: {
    sendEmail: (e) => {
      emailjs.sendForm('nadeemkhanrtm_360', 'template_ke3v59q', e.target, 'user_y5BOqp4dGHEX5NMsjzkzk')
        .then((result) => {
            console.log('SUCCESS!', result.status, result.text);
        }, (error) => {
            console.log('FAILED...', error);
        });
    }
  }

};
</script>

<style scoped></style>
