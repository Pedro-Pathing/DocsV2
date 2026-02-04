<template>
  <MDCSlot :code="code" lang="groovy" />
</template>

<script setup>
const latestVersion = ref('x.y.z')

onMounted(async () => {
  try {
    const response = await fetch('https://api.github.com/repos/Pedro-Pathing/PedroPathing/releases/latest')
    const data = await response.json()
    latestVersion.value = data.tag_name.slice(1)
  } catch (error) {
    console.error(error)
  }
})

const code = computed(() => 
  `implementation 'com.pedropathing:ftc:${latestVersion.value}'
implementation 'com.pedropathing:telemetry:1.0.0'`
)
</script>
