@@ -1,28 +1,26 @@
<template>
   <div>
    <h1>New participant</h1>
     Firstname<input type="text" v-model="Firstname"><br>
    Lastname<input type="text" v-model="Lastname"><br>
    <button @click="addNew()">Add new participant</button>
    <!-- <new-participant-form @added="addNewParticipant($event)"></new-participant-form> -->
    <h1>Participants list</h1>
    <participants-form @added="addNew($event)"></participants-form>
   <participants-list :list="list"></participants-list>
    </div>
</template>


<script>
import ParticipantsList from "./ParticipantsList.vue";
import NewParticipantsList from "./NewParticipantsList.vue";
import ParticipantsForm from "./ParticipantsForm.vue";
    export default {
      components: {ParticipantsList, NewParticipantsList},
      components: {ParticipantsList, ParticipantsForm},
        data() {
            return {list: [],
            Firstname: "",
            Firstname: "" ,
            Lastname: ""}
        },
        methods: {
          addNew() {
             this.list.push(this.Firstname + this.Lastname);
             this.ParticipantsList
          addNew(Person) {
            console.log(Person);
             this.list.push(Person);
          }
        }
    };
