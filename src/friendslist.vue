<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <ol>
        <li v-for="person in participants">
        {{person.firstname}}
        {{person.lastname}}
        </li>
      </ol>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text" v-model="newParticipant.firstname">
      <label>Lastname</label>
      <input type="text" v-model="newParticipant.lastname">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {
	participants:[{firstname: "John", lastname:"Doe"}],
	newParticipant:{},
	};
    },
    methods: {
      addNewParticipant() {
        this.participants.push(this.newParticipant);
        this.newParticipant = {};
      }
    }
  };
</script>

<template>
  <div>  
    <h1>{{ title }}</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>
 
<script>
    export default {
        data() {
            return {title: 'Not clicked yet'}
        },
        methods: {
            iAmClicked() {
                this.title = 'Clicked';
            }
        }
    };
</script>

