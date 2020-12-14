<template>
  <div class="bg-gray-300 h-screen">
    <Intro/>
    <SelectCountryStateCity/>
  </div>
</template>

<script>

import Intro from "./components/Main";
import SelectCountryStateCity from "./components/SelectContryStateCity";
 export default {
   name:'App',
   components:{
     Intro,
     SelectCountryStateCity
   }
 }
</script>

<style>

</style>
