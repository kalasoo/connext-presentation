<template lang="jade">
section
    h1 {{title}}
    .content(v-html='content | marked')
</template>

<script lang="babel">
let marked = require('marked');
module.exports = {
    filters: {
        marked: marked
    }
}
</script>