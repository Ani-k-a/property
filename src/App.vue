<template>
  <div>
    <h2>{{ text }}</h2>
    <!-- <input type="text" v-model="text" /> -->
    <CustomInput v-model="text" />
    <ApartmentsList :items="apartments">
      <template v-slot:title>New title 123</template>
      <template v-slot:apartment="{ apartment }">
        <ApartmentsItem
          @click="handleItemclick"
          :key="apartment.id"
          :description="apartment.descr"
          :rating="apartment.rating"
          :imgUrl="apartment.imgUrl"
          :price="apartment.price"
        />
      </template>
    </ApartmentsList>
  </div>
</template>

<script>
import ApartmentsList from "./components/apartment/ApartmentsList.vue";
import ApartmentsItem from "./components/apartment/ApartmentsItem.vue";
import apartments from "./components/apartment/apartments";
import CustomInput from "./components/shared/CustomInput.vue";
export default {
  name: "App",
  components: {
    ApartmentsList,
    ApartmentsItem,
    CustomInput,
  },
  data() {
    return {
      text: " ",
      apartments,
    };
  },
  methods: {
    handleItemclick() {
      console.log("item click");
    },
  },
};
</script>

<style>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 60px;
}
</style>
