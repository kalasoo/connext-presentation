<style lang="sass">
$normal: #777;
$dark: #333;
$blue: #5D94C8;
section {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    height: 100%;
    padding: 10%;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
    background-attachment: fixed;
    & > .page {
        opacity: .5;
        position: absolute;
        bottom: .5em;
        right: .5em;
        transition: opacity .3s;
        &:hover {
            opacity: 1;
        }
    }
    img, video {
        max-width: 100%;
    }
}
hr {
    border: none;
    width: 30%;
    margin: 2em auto;
    border-bottom: 2px dotted $blue;
}
blockquote {
    font-size: .8em;
    text-align: left;
    color: $dark;
    background: $blue * .1 + #fff * .9;
    padding: .5em 1.5em;
}
.title {
    background: #fff;
}
.content {
    margin: 2em 0;
}
</style>

<template lang="jade">
section(style='{{!!background ? "background-image: url(" + background + ")" : ""}}')
    .inner
        h1.title {{title}}
        .content(v-html='content | marked')
    .page {{$index + 1}}/{{pagesLength}}
</template>

<script lang="babel">
let marked = require('marked');
module.exports = {
    props: ['pagesLength'],
    filters: {
        marked: marked
    }
}
</script>