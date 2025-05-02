<template>
  <p v-for="(user, index) in users1" :key="user"> 
    {{ index }} {{ user }}
  </p>

  <br>

  <p v-for="(user, index) in users2" :key="user.email">
    {{ index }} {{ user.name }} {{ user.email }}
  </p>

  <br>

  <div v-for="(user, index) in users2" :key="user.email">
    <p v-if="user.name === 'usrC'"> 
      Index #{{ index }}
      named {{ user.name }}
      has an email address: {{ user.email }}
    </p>

  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      users1: ['usrA', 'usrB', 'usrC'],
      users2: [
        { name: 'usrA', email: 'aaa@aaa' },
        { name: 'usrB', email: 'bbb@bbb' },
        { name: 'usrC', email: 'ccc#ccc' },
      ],
    }; 
  },
};
</script>
