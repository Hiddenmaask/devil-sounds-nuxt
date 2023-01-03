<template class="">
  <div class="bg-white dark:bg-gray-800 h-full justify-center grid">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>

</template>

<script>




export default {
  name: "app",


}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

@tailwind base;
@tailwind components;
@tailwind utilities;



*, *::after, *::before {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

button {
  font: inherit;
  border:none;
  cursor: pointer;
}

input,
label {
  font: inherit;
}

@-ms-viewport{
  width: device-width;
}

html,body{
  height: 100%;
}

html{
  font-size: 62.5%;
}

#__nuxt{
  scroll-behavior: smooth;
  height: 100%;
}

body {
  font-family: 'Poppins', sans-serif;
  font-size: 1.6rem;
  line-height: 1.6;
  color: #fff;
  background-color: #fff;
}


h1,h2,h3,h4,h5,h6{
  font-family: 'Poppins', sans-serif;
  font-weight: 700;
}

h1{
  font-size: 3.6rem;
}

h2{
  font-size: 3.2rem;
}

h3{
  font-size: 2.8rem;
}

h4{
  font-size: 2.4rem;
}

@layer components{
  .btn{
    @apply bg-indigo-500 p-2 rounded-md w-full text-white hover:bg-indigo-800 transition-all duration-300 ease-linear cursor-pointer;
  }

  .form-input{
    @apply rounded-md shadow-sm block w-full placeholder:italic placeholder:text-slate-400 autofill:bg-slate-200 p-3 ;
  }

  .input-wrapper{
    @apply inline-flex p-2 bg-indigo-500 rounded-md shadow-lg;

  }

  input{
    @apply focus:bg-slate-200 active:bg-slate-200 focus:ring-1 focus:ring-indigo-800 active:ring-1 active:ring-indigo-800 ring-offset-2 outline-none transition-all duration-300 ease-linear;
  }

  .card{
    @apply grid gap-6 bg-white drop-shadow-2xl  dark:bg-gray-800 rounded-lg px-6 py-8 ring-1 ring-slate-900/5 shadow-xl text-black dark:text-white m-4;
  }
}

</style>
