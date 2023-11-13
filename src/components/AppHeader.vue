<template>
    <header class="d-flex align-items-center">
        <h1>Yu-Gi-Oh Api</h1>
    </header>
</template>

<script>
export default {
    name: 'AppHeader'

}
</script>

<style lang="scss">
@use '../assets/styles/partials/varaiables' as *;
@use '../assets/styles/partials/mixins' as *;

header {
    height: 80px;
    padding: 30px;
}
</style>