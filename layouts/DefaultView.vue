<template>
  <div>
    <PartialTheHeader :links-menu="linksMenu" />
    <div class="container mx-auto">
      <Nuxt />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      linksMenu: [
        {
          link: 'https://github.com/',
          label: 'GitHub',
        },
        {
          link: 'https://google.fr',
          label: 'Google',
        },
      ],
    }
  },
}
</script>
