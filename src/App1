<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <ol>
        <li v-for="person in participants">
          {{ person.firstname }} {{ person.lastname }}
        </li>
      </ol>
    </div>

    <h3>New participant</h3>
    <new-participant-form @added="addNewParticipant($event)"></new-participant-form>
  </div>
</template>

<script>
  import NewParticipantForm from "./NewParticipantForm.vue";

  export default {
    components: {NewParticipantForm},
    data() {
      return {
        participants: [
          {firstname: "John", lastname: "Doe"}, 
          {firstname: "Robin ", lastname: "Hood"}, 
          {firstname: "Chuck ", lastname: "Norris"}, 
          {firstname: "Kate ", lastname: "Flower"}, 
        ]
      };
    },
    methods: {
      addNewParticipant(newParticipant) {
        this.participants.push(newParticipant);
      }
    }
  };
</script>
