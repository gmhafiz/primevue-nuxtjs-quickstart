<template>
  <div class="container">
    <div>
      <Logo />
      <Toast />

      <form @submit.prevent="greet">
        <InputText v-model="text" type="text" />
        <Button type="submit" label="Submit" />
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      text: null
    }
  },
  methods: {
    greet () {
      this.$toast.add({ severity: 'info', summary: 'Hello ' + this.text })
    }
  }
}
</script>

<style>
.container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
