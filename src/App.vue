@@ -1,28 +1,26 @@
<template>
   <div>
    <h1>New participant</h1>
    <!-- <new-participant-form @added="addNewParticipant($event)"></new-participant-form> -->
    <h1>Participants list</h1>
    <participants-form @added="add_new_person($event)"></participants-form>
    <participants-list :list="list"></participants-list>
    </div>
</template>


<script>
import ParticipantsList from "./components/ParticipantsList.vue";
import ParticipantsForm from "./components/ParticipantsForm.vue";

    export default {
      components: {
          "ParticipantsForm": ParticipantsForm,
          "ParticipantsList": ParticipantsList
        },
        data() {
            return {list: [],
            Firstname: "" ,
            Lastname: ""}
        },
        methods: {
          add_new: function() {
             this.list.push(this.Firstname + ' ' + this.Lastname);
          },
          add_new_person: function(Person) {
             this.list.push(Person);
          }
        }
    };
    </script>
