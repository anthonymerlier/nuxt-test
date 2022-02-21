<template>
  <button :id="customId" type="button" :class="getClass(bgColor, textColor)">
    Get started
  </button>
</template>

<script>
export default {
  props: {
    customId: {
      type: String,
      required: true,
    },
    bgColor: {
      type: String,
      required: true,
    },
    textColor: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      getClass: (bgColor, textColor) => {
        return `ext-white bg-${bgColor}-700 hover:bg-${bgColor}-800 focus:ring-4 focus:ring-${bgColor}-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center mr-3 md:mr-0 dark:bg-${bgColor}-600 dark:hover:bg-${bgColor}-700 dark:focus:ring-${bgColor}-800 text-${textColor}`
      },
    }
  },
}
</script>
