@ -0,0 +1,26 @@
<template>
  <div>
    <form @submit.prevent="add()">
     Firstname<input type="text" v-model="Firstname"><br>
    Lastname<input type="text" v-model="Lastname"><br>
    <button>Add new participant</button>
    </form>
  </div>
</template>


<script>
  export default {
    data() {
      return {newParticipant: {},
      Firstname: "" ,
      Lastname: ""
    }},
    methods: {
      add() {
        this.$emit('added', this.Firstname +' '+ this.Lastname);
        this.newParticipant = {};
      }
    }
  };
</script>
