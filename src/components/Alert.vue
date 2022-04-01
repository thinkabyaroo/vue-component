<template>
  <div>
    <h3 :class="['alert',color]">
      <input v-model="message" type="text" @keyup.enter="edit" class="form-control" v-if="isEdit">

      <span v-else @dblclick="edit">
              {{message}}
      </span>
      <div v-if="isLoading" class="spinner-border text-dark" role="status">
        <span class="visually-hidden">Loading...</span>
      </div>
    </h3>
  </div>
</template>

<script>
export default {
  name:"Alert",
  props: {
    message: {
      type: String,
      default: "Say Something"
    },
    color:{
      type:String,
      default: "alert-danger"
    }
  },
  data() {
    return {
      isLoading: false,
      isEdit:false
    }
  },
  methods: {
    edit() {
      this.isEdit= !this.isEdit
    }
  },
}
</script>

<style scoped>

</style>