<template>
  <div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 text-center pt-10 ">
      <h1 v-if="err" class="col-span-3">Cannot Fetch Data Plz reload</h1>
      <div>
        <label for="country" class="text-xl text-pink-800 mr-5"
          >Select Country</label
        >
        <select
          class="w-6/12 p-3 text-pink-800"
          v-model="selectedCountry"
          id="country"
        >
          <option selected disabled>Coutry</option>
          <option>India</option>
        </select>
      </div>

      <div>
        <label for="state" class="text-xl text-pink-800 mr-5"
          >Select State</label
        >
        <select
          class="w-6/12 p-3 text-pink-800"
          v-model="selectedState"
          id="state"
        >
          <option selected disabled>State</option>
          <template v-if="selectedCountry === 'India'">
            <option v-for="state in arrState" v-bind:key="state.id">{{
              state
            }}</option>
          </template>
        </select>
      </div>

      <div>
        <label for="city" class="text-xl text-pink-800 mr-5"
          >Select City
        </label>
        <select
          class="w-6/12 p-3 text-pink-800"
          v-model="selectedCity"
          id="city"
        >
          <option selected disabled>City</option>
          <template v-if="selectedState === 'Maharashtra'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Karnataka'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Andhra Pradesh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Tamil Nadu'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Kerala'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Delhi'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Uttar Pradesh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'West Bengal'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Odisha'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Rajasthan'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Telangana'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Chhattisgarh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Bihar'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Haryana'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Assam'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Gujarat'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Madhya Pradesh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Punjab'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Jammu and Kashmir'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Jharkhand'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Uttarakhand'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Goa'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Himachal Pradesh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Puducherry'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Tripura'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Manipur'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Chandigarh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Arunachal Pradesh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Meghalaya'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Nagaland'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Ladakh'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Sikkim'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Andaman and Nicobar Islands'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Mizoram'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Daman and Diu'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Dadra and Nagar Haveli'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
          <template v-if="selectedState === 'Lakshadweep'">
            <option v-for="city in arrCity" v-bind:key="city.id">
              {{ city }}
            </option>
          </template>
        </select>
      </div>
      <!--
      <span class="selectedCountry">{{ selectedCountry }}</span>

      <span>{{ selectedState }}</span>

      <span>{{ selectedCity }}</span>

      <span>State Active {{ stateActive }}</span>

      <span>State Confirmed {{ stateConfirmed }}</span>

      <span>State Deaths {{ stateDeaths }}</span>

      <span>City Confirmed {{ cityConfirmed }}</span>
    --></div>

    <data-show :selectedCity="selectedCity"
     :cityConfirmed="cityConfirmed"
      :stateActive="stateActive" 
      :stateConfirmed="stateConfirmed" 
      :stateDeaths="stateDeaths" 
      :stateRecovered="stateRecovered"
      :selectedState="selectedState"></data-show>
  </div>
</template>

<script>
import axios from "axios";
import DataShow from "./DataShow.vue";

export default {
  components: {
    "data-show": DataShow,
  },
  name: "SelectCountryStateCity",

  data() {
    return {
      selectedCountry: "",
      selectedState: "",
      selectedCity: "",
      dataSet: [] /* all data of API saved in it for reusable */,
      arrState: [],
      arrCity: [],
      err: "",
      stateActive: "",
      stateConfirmed: "",
      stateDeaths: "",
      stateRecovered: "",
      stateActiveChanges: "",
      stateConfirmedChanges: "",
      stateDeathsChanges: "",
      stateRecoveredChanges: "",
      cityConfirmed: "",
    };
  },
  created() {
    axios
      .get("https://api.covidindiatracker.com/state_data.json")
      .then((data) => {
        this.dataSet = data.data;
      })
      .catch((err) => (this.err = err));
  },
  beforeUpdate() {
    this.arrState = [];
    this.arrCity = [];
    this.stateActive,
      this.stateConfirmed,
      this.stateDeaths,
      this.cityConfirmed,
      this.stateRecovered,
      this.stateActiveChanges,
      this.stateConfirmedChanges,
      this.stateDeathsChanges,
      this.stateRecoveredChanges = "";
    this.dataSet.forEach((values) => {
      if (this.selectedCountry === "India") {
        this.arrState.push(values.state);
      }
      if (values.state === this.selectedState) {
        this.stateActive = values.active;
        this.stateConfirmed = values.confirmed;
        this.stateDeaths = values.deaths;
        this.stateRecovered = values.recovered;
        values.districtData.forEach((city) => {
          this.arrCity.push(city.name);
          if (this.selectedCity === city.name) {
            console.log(city.confirmed)
            this.cityConfirmed = city.confirmed;
          }
        });
      }
    });
  },
};
</script>

<style scoped>
.selectedCountry {
  opacity: 1;
  transition: opacity 2s linear;
}

.selectedCountry:hover {
  opacity: 0;
}

/* width */
::-webkit-scrollbar {
  width: 2px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px rgba(157, 23, 77, 1);
  border-radius: 10px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: rgba(157, 23, 77, 1);
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: rgba(157, 23, 77, 1);
}
</style>
