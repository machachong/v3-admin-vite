<script lang="ts" setup>
import { useUserStore } from "@/store/modules/user"
import Admin from "./components/Admin.vue"
import Editor from "./components/Editor.vue"
import HelloWorld from "../../../ProTable/src/components/HelloWorld.vue"

const userStore = useUserStore()
const isAdmin = userStore.roles.includes("admin")
</script>

<template>
  <component :is="isAdmin ? Admin : Editor" />
  <HelloWorld />
</template>
