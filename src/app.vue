<style lang="sass">
$normal: #777;
$dark: #333;
$blue: #5D94C8;
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
    font-size: 20px;
    color: $normal;
}
h1, h2, h3, h4, h5, h6, strong {
    color: #333;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
}
section {
    text-align: center;
    height: 100%;
    padding: 10%;
    &:nth-child(2n + 1) {
        background-image: radial-gradient(circle at 50% 50%, rgba(#f1f1f1, .1), #ddd);
    }
}
a {
    color: $blue;
    text-decoration: none;
}
hr {
    border: none;
    height: 2px;
    width: 30%;
    margin: 2em auto;
    background-color: $blue;
}
.content {
    margin: 2em 0;
}
</style>

<template lang="jade">
section-view(v-repeat='sections')

</template>

<script lang="babel">
let sections = [
    {
        title: '为什么我们需要一个更好的技术分享方式？',
        content: `
![cover](./images/favicon.ico)

阴明 - [稀土](https://xitu.io) & [掘金](http://gold.xitu.io)

[ming@xitu.io](mailto://ming@xitu.io)
        
2015年7月19日
        `,
    },
    {
        title: '经历',
        content: `
信息工程 @ 香港中文大学

计算机科学 @ 剑桥大学

Researcher => Developer

------

Founder & Frontend Developer @ GradChef.com

**Founder & Frontend Developer @ xitu.io**

        `
    }
]

import section from './components/section.vue'

export default {
    replace: false,
    data () {
        return {
            sections: sections,
            currentIndex: 0
        }
    },
    components: {
        'section-view': section
    }
}

</script>