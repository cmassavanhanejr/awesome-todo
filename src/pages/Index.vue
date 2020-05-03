<template>
  <q-page padding>
    <input
      v-model="message"
      @keyup.esc="clearMessage"
      @keyup.enter="alertMessage"
      />
      <!--@keyup_enter="alertMessage"-->
    <button @click="clearMessage" >clear</button>
    <h5 class="border-grey">{{message}}</h5>
  </q-page>
</template>

<script>
export default {
  data () {
    return {
      message: 'Hello World Vue!'
    }
  },
  methods: {
    clearMessage () {
      this.message = ''
    },
    alertMessage () {
      alert(this.message)
    }
    /* handleKeyup (e) {
      console.log(e)
      if (e.keyCode === 27) {
        this.clearMessage()
      } else if (e.keyCode === 13) {
        this.alertMessage()
      }
    } */
  }
}
</script>

<style>
 .border-grey{
   border: 1px solid grey;
 }
</style>
