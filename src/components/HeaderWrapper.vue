<template>
  <header class="text-gray-600 body-font">
    <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
      <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          class="w-10 h-10 text-white p-2 bg-indigo-500 rounded-full"
          viewBox="0 0 24 24"
        >
          <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path>
        </svg>
        <span class="ml-3 text-xl">Vue Project</span>
      </a>
      <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
        <router-link to="/" class="mr-5 hover:text-gray-900">Home</router-link>
        <router-link to="/profile" class="mr-5 hover:text-gray-900">User Profile</router-link>
        <router-link to="/items" class="mr-5 hover:text-gray-900">Items</router-link>
      </nav>
      <button
      @click="logOut"
        class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0"
      >
        Logout
      </button>
    </div>
  </header>
  <slot />
</template>

<script>
export default {
  data() {
    return {

    };
  },
  methods: {
    logOut(){
      this.$store.dispatch('logOut');
      this.$router.push('/login')
    }
  }
}
</script>