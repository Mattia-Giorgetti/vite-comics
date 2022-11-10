<template>
    <section>
        <div class="container">
            <h2>--Content Goes Here--</h2>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'ContentSectionComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

section {
    background-color: black;
    height: 140px;

    h2 {
        color: white;
        line-height: 115px;
        padding: 0;
    }
}

</style>