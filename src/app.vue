<style lang="sass">
body {
    margin: 0;
    font-family: 'Hiragino Sans GB', sans-serif;
}
.container {
    max-width: 600px;
    margin: 0 auto;
}
section {
    padding: 5em 0;
}

</style>

<template lang="jade">
.container
    section 1

    section 2

    section 3

</template>

<script lang="babel">
import section from './components/section.vue'

export default {
    replace: false,
    data () {

    }
}

</script>