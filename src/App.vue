<template>
   <div>
    <h1>New participant</h1>
     Firstname<input type="text" v-model="Firstname"><br>
    Lastname<input type="text" v-model="Lastname"><br>
    <button @click="addNew()">Add new participant</button>
    <!-- <new-participant-form @added="addNewParticipant($event)"></new-participant-form> -->
   <participants-list :list="list"></participants-list>
    </div>
</template>

<script>
import ParticipantsList from "./ParticipantsList.vue";
import NewParticipantsList from "./NewParticipantsList.vue";
    export default {
      components: {ParticipantsList, NewParticipantsList},
        data() {
            return {list: [],
            Firstname: "",
            Lastname: ""}
        },
        methods: {
          addNew() {
             this.list.push(this.Firstname + this.Lastname);
             this.ParticipantsList
          }
        }
    };
</script>