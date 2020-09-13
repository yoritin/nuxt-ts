<template>
  <div>
    <UserData :user="user" />
  </div>
</template>

<script>
import UserData from '@/components/UserData'

export default {
  components: {
    UserData
  },

  data() {
    return {
      user: {
        firstName: 'makoto',
        lastName: 'katayori'
      }
    }
  }
}
</script>