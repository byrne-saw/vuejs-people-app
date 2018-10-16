<template>
  <div class="home">
    
     <h1>Interesting Peeps: {{this.people.length}}</h1>

        <ul>
          <li v-for="person in people" v-on:click="" v-if="">{{person.name}}: {{person.bio}}</li>
        </ul>

        <div>
          Name: <input v-model="newPerson.name">
          Bio: <input v-model="newPerson.bio">
          <button v-on:click="addPerson()">Add person</button>
        </div>


  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  data: function() {
    return {
      people: [
              {name: "Kek", bio: "The one and only", bioVisible: true},
              {name: "Whypler", bio: "an unfortunate series of events", bioVisible: true},
              {name: "scrod", bio: "better left unsaid", bioVisible: true}
              ],
      newPerson: {name: "", bio: "", bioVisible: true}
    };
  },
  created: function() {},
  methods: {
    addPerson: function() {
      this.people.push(this.newPerson);
      this.newPerson = {name: "", bio: "", completed: false};
    }
  },
  computed: {}
};
</script>