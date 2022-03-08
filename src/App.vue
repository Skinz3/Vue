<template>
  <div class="center">
    <vs-button :active="active == 0" @click="active = 0">Active</vs-button>
    <vs-button :active="active == 1" @click="active = 1">Default</vs-button>
    <vs-button disabled>Disabled</vs-button>
     <template>
    <vs-button @click="openLoading">Open Loading</vs-button>
  </template>
  </div>
</template>

<script>


export default {
      methods: {
        openLoading() {
          const loading = this.$vs.loading()
          setTimeout(() => {
            loading.close()
          }, 3000)
        }
      }
    };
 

</script>

<style>
.center {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}
</style>
