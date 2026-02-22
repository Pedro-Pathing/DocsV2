<template><pre class="shiki shiki-themes github-light github-dark-dimmed" style="padding: 1rem; border-radius: 0.5rem; overflow-x: auto; margin: 1rem 0;"><code style="font-family: 'Monaco', 'Menlo', 'Consolas', monospace; font-size: 0.875rem; line-height: 1.7; white-space: pre;">{{ code }}</code></pre></template>

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
