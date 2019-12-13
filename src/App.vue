@@ -1,28 +1,26 @@
<template>
   <div>
    <h1>New participant</h1>
    <!-- <new-participant-form @added="addNewParticipant($event)"></new-participant-form> -->
    <h1>Participants list</h1>
    <participants-form @added="addNew($event)"></participants-form>
   <participants-list :list="list"></participants-list>
    </div>
</template>


<script>
import ParticipantsList from "./ParticipantsList.vue";
import ParticipantsForm from "./ParticipantsForm.vue";
    export default {
      components: {ParticipantsList, ParticipantsForm},
        data() {
            return {list: [],
            Firstname: "" ,
            Lastname: ""}
        },
        methods: {
          addNew() {
             this.list.push(this.Firstname + ' ' + this.Lastname);
          addNew(Person) {
            console.log(Person);
             this.list.push(Person);
          }
        }
    };
