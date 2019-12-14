@ -0,0 +1,16 @@
<template>
  <div>
    <ol>
        <li v-for="(person, index) in list" :key="person.Lastname" :value="person.Lastname">
          {{person}}
          <button v-on:click="remove(index)">Remove</button>
        </li>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list'],
    methods: {
      remove: function(index){
          this.list.splice(index, 1);
      }
    }
  };
</script>
