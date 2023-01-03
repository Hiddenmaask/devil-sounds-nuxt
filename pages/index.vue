<template>

  <div class="dark justify-center flex m-20 ">

    <!-- form for login -->
    <form class="login-form card" @submit.prevent="login">
      <h2>login</h2>
      <div class="input-wrapper">

        <input
            type="text"
            placeholder="email"
            id="email"
            class="form-input"
        >
      </div>
      <div class="input-wrapper">

        <input
            type="password"
            placeholder="password"
            id="password"
            class="form-input "
        >
      </div>
      <div class=" flex right-0 ">
        <!-- remember me checkbox -->
        <label
            for="remember"
            class="form-label">
          remember me</label>
        <input
            type="checkbox"
            id="remember"
            class="checked:bg-blue-500 p-2 rounded-md shadow-sm block p-2"
        >

      </div>

      <div class="">
        <NuxtLink to="/dashboard">
          <button
              type="submit"
              class="btn">
            <h4>login</h4>
          </button>
        </NuxtLink>
        <div class="info-box flex ">
          <p class="text-center text-slate-500 font-bold">Don't have an account? <a href="/register" class="text-blue-500 hover:text-indigo-300">Register</a></p>

        </div>
      </div>
    </form>

    <!-- link to about page -->
  </div>

</template>

<script>
import { mapMutations } from 'vuex'
definePageMeta({
  layout: "custom",
});
export default {
  name: "index",
  head() {
    return {
      title: "Home Page",
    }
  },
  asyncData() {
    return {
      rendering: process.server ? 'server' : 'client'
    }
  }


}

</script>

<style scoped>



</style>
