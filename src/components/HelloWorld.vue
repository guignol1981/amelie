<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div>
    <img
      class="h-44 w-full object-cover lg:h-64"
      :src="profile.backgroundImage"
      alt=""
    />
  </div>
  <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="-mt-12 sm:-mt-16 sm:flex sm:items-end sm:space-x-5">
      <div class="flex">
        <img
          class="h-24 w-24 rounded-full ring-4 ring-white sm:h-32 sm:w-32 object-cover"
          :src="profile.avatar"
          alt=""
        />
      </div>
      <div
        class="mt-6 sm:flex-1 sm:min-w-0 sm:flex sm:items-center sm:justify-end sm:space-x-6 sm:pb-1"
      >
        <div class="sm:hidden md:block mt-6 min-w-0 flex-1">
          <h1 class="text-2xl font-bold text-gray-900 truncate">
            {{ profile.name }}
          </h1>
        </div>
        <div
          class="mt-6 flex flex-col justify-stretch space-y-3 sm:flex-row sm:space-y-0 sm:space-x-4"
        >
          <button
            type="button"
            class="inline-flex justify-center px-4 py-2 border border-gray-300 shadow-sm text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-pink-500"
          >
            <MailIcon
              class="-ml-1 mr-2 h-5 w-5 text-gray-400"
              aria-hidden="true"
            />
            <span>Message</span>
          </button>
          <button
            type="button"
            class="inline-flex justify-center px-4 py-2 border border-gray-300 shadow-sm text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-pink-500"
          >
            <PhoneIcon
              class="-ml-1 mr-2 h-5 w-5 text-gray-400"
              aria-hidden="true"
            />
            <span>Call</span>
          </button>
        </div>
      </div>
    </div>
    <div class="hidden sm:block md:hidden mt-6 min-w-0 flex-1">
      <h1 class="text-2xl font-bold text-gray-900 truncate">
        {{ profile.name }}
      </h1>
    </div>
  </div>
</template>

<script>
import { MailIcon, PhoneIcon } from "@heroicons/vue/solid";

const profile = {
  name: "Amelie Legare",
  email: "amelielegare@gmail.com",
  avatar:
    "https://scontent.fyhu2-1.fna.fbcdn.net/v/t39.30808-6/237069721_10159778825337193_4496134688929673643_n.jpg?_nc_cat=100&ccb=1-5&_nc_sid=09cbfe&_nc_ohc=Me4faRH1St8AX-BhPNC&_nc_ht=scontent.fyhu2-1.fna&oh=4438e8dbf673e586cfa0ea6444dc1c55&oe=613B8C33",
  backgroundImage:
    "https://images.unsplash.com/photo-1457369804613-52c61a468e7d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1650&q=80",
  fields: [
    ["Phone", "(555) 123-4567"],
    ["Email", "ricardocooper@example.com"],
    ["Title", "Senior Front-End Developer"],
    ["Team", "Product Development"],
    ["Location", "San Francisco"],
    ["Sits", "Oasis, 4th floor"],
    ["Salary", "$145,000"],
    ["Birthday", "June 8, 1990"],
  ],
};

export default {
  components: {
    MailIcon,
    PhoneIcon,
  },
  setup() {
    return {
      profile,
    };
  },
};
</script>
