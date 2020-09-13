<template>
  <div>
    <UserData :user="user" />
  </div>
</template>

<script lang="ts">
import UserData from '~/components/UserData.vue'

interface User {
  firstName: string
  lastName: string
}

export default {
  components: {
    UserData
  },

  data(): { user: User } {
    return {
      user: {
        firstName: 'makoto',
        lastName: 'katayori'
      }
    }
  }
}
</script>