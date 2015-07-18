<style lang="sass">
* {
    box-sizing: border-box;
}
html {
    height: 100%;
}
body {
    height: 100%;
    margin: 0;
    font-family: 'Source Code Pro', 'Hiragino Sans GB', sans-serif;
    font-weight: 300;
}
section {
    height: 100%;
    padding: 10%;
    &:nth-child(2n) {
        background-color: rgba(#f1f1f1, .5);
    }
}

</style>

<template lang="jade">
section-view(
    v-repeat='section: sections',
    title='section.title',
    content='section.content'
)

</template>

<script lang="babel">
let sections = [
    {
        title: '我是',
        content: '# 阴明',
    },
    {
        title: '经历',
        content: '### 悲剧'
    }
]

import section from './components/section.vue'

export default {
    replace: false,
    data: {
        sections: sections
    },
    components: {
        'section-view': section
    }
}

</script>