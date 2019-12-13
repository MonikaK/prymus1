@ -0,0 +1,16 @@
<template>
  <div>
    <ol>
        <li v-for="person in list">
          {{person}}
          <button>Remove</button>
        </li>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list']
  };
</script>
