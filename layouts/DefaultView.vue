<template>
  <div>
    <PartialTheHeader :links-menu="linksMenu" />
    <div class="container mx-auto py-5">
      <h1 class="py-5">{{ title }}</h1>
      <slot></slot>
    </div>
    <PartialTheFooter />
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      linksMenu: [
        {
          link: '/',
          label: 'Home',
        },
        {
          link: '/about',
          label: 'About',
        },
      ],
    }
  },
}
</script>

<style>
h1 {
  font-size: 36px;
  font-weight: bold;
}
</style>
