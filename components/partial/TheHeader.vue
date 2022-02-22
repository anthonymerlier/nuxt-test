<template>
  <nav
    class="bg-gray-200 border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-800"
  >
    <div class="container flex flex-wrap justify-between items-center mx-auto">
      <a href="#" class="flex">
        <span
          class="self-center text-lg font-semibold whitespace-nowrap dark:text-white"
          >Nuxt JS App</span
        >
      </a>
      <div class="flex md:order-2">
        <ButtonBtnClassic
          custom-id="ctaButton"
          bg-color="green"
          text-color="white"
          label="Button"
          link="https://github.com/"
        />
        <ButtonBtnToggleMenu />
      </div>
      <div
        id="mobile-menu-4"
        class="hidden justify-between items-center w-full md:flex md:w-auto md:order-1"
      >
        <ul
          class="flex flex-col mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium"
        >
          <li v-for="(item, index) in linksMenu" :key="index">
            <nuxtLink
              class="block py-2 pr-4 pl-3 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white"
              aria-current="page"
              :to="item.link"
              >{{ item.label }}</nuxtLink
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    linksMenu: {
      type: Array,
      required: true,
    },
  },
}
</script>
