<template>
  <div class="form-container fixed h-screen w-screen flex justify-center bg-[#f6aec3] ">
    <form action="">
      <h2 class="text-4xl text-center text-white mt-16 select-none">Register</h2>
      <div class="flex justify-center items-center">
        <img class="w-48 select-none" src="../../assets/image/cute_heart.png" alt="" />
      </div>
      <div>
        <div>
         <span class="ml-3 text-red-600">{{ firstNameMes }}</span><br>
          <input type="text" v-model="firstName" placeholder="  First name"  :style="{ border: borderFirstName }" />
        </div>
        <div>
          <span class="ml-3 text-red-600">{{ lastNameMes }}</span><br>
          <input type="text" v-model="lastName" placeholder="  Last name"  :style="{ border: borderLastName }"/>
        </div>
        <div>
          <span class="ml-3 text-red-600" >{{ phoneNumberMes }}</span><br>
          <input type="number" v-model="phoneNumber"  placeholder="  Phone number" :style="{ border: borderPhoneNum}"/>
        </div>
        <div>
            <button class="bg-red-600 text-white border border-white select-none" @click.prevent="playerRegiser">Submit</button>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped>
input[type = "text"],input[type = "number"],button {
  margin: 10px;
  padding: 7px;
  width:20.8rem;
  border-radius:10px;
}
</style>

<script setup lang="ts">
  import { ref } from 'vue';
  const firstName = ref('');
  const lastName = ref('');
  const phoneNumber = ref('');
  const firstNameMes = ref('');
  const lastNameMes = ref('');
  const phoneNumberMes = ref('');
  const borderPhoneNum = ref('');
  const borderFirstName =  ref('');
  const borderLastName = ref('');
  const playerRegiser = () => {
    if (firstName.value === '') {
      firstNameMes.value = 'First name required';
      borderFirstName.value = '2px solid red';
    } else {
      firstNameMes.value = '';
      borderFirstName.value = '';
    }
    if (lastName.value === '') {
      lastNameMes.value = 'Last name required';
      borderLastName.value = '2px solid red';
    }else {
      lastNameMes.value = '';
      borderLastName.value = '';
    }
    if (phoneNumber.value === '') {
      phoneNumberMes.value = 'Phone number required';
      borderPhoneNum.value = '2px solid red';

    }else {
      phoneNumberMes.value = '';
      borderPhoneNum.value = ''
    }
  }
</script>
