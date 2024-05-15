<template>
  <div class="form-container h-screen w-screen flex justify-center bg-pink-400">
    <form action="">
      <h2 class="text-4xl text-center text-white mt-16">Register</h2>
      <div class="flex justify-center items-center">
        <img class="w-48" src="../../assets/image/cute_heart.png" alt="" />
      </div>
      <div>
        <div>
          <input type="text" placeholder="  First name" />
        </div>
        <div>
          <input type="text" placeholder="  Last name" />
        </div>
        <div>
          <input type="text" placeholder="  Phone number" />
        </div>
        <div>
            <button class="bg-red-600 text-white border border-white">Submit</button>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped>
input[type = "text"],button {
  margin: 10px;
  padding: 7px;
  width:20.8rem;
  border-radius:20px;
}
input {
    border:2px solid red;
}
</style>
