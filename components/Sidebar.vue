<template>
  <v-navigation-drawer
    v-model="drawerState"
    :fixed="fixed"
    app
  >
    <v-list>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :to="item.to"
        router
        exact
      >
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title v-text="item.title" />
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script lang="ts">
export default {
  props: {
    drawer: {
      type: Boolean,
      default: false
    },
    fixed: {
      type: Boolean,
      default: false
    },
    items: {
      type: Array
    }
  },
  data() {
    return {
      drawerState: this.drawer
    }
  },
  watch: {
    drawer() {
      this.drawerState = !this.drawerState
    }
  }
}
</script>