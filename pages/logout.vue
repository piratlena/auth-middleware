<template>
  <div>
    <h2>Logout</h2>
  </div>
</template>

<script setup>

definePageMeta({
  middleware: function (to, from){
    const user = useCookie('user')
    user.value = null
    return navigateTo('/login')
  }
})

</script>