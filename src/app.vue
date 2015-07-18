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
    &::-webkit-scrollbar {
        width: 1em;
    }
    &::-webkit-scrollbar-track {
        background: rgba($normal, .2);
    }
    &::-webkit-scrollbar-thumb {
        background: $blue;
    }
}
h1, h2, h3, h4, h5, h6, strong {
    color: #333;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
}
a {
    color: $blue;
    text-decoration: none;
}
</style>

<template lang="jade">
section-view(v-repeat='sections', pages-length='{{totalLength}}')

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

[more](http://ming.today/timeline)        `
    },
    {
        title: 'LAMP',
        content: `
所有人共通的学习经历

Linux / Apache / MySQL / PHP

------

面对一个初学者，这个世界并不友善
`
    },
    {
        title: '信息在爆炸',
        background: './images/growth.png',
        content: `
除了层出不穷的框架、知识

在我们面前的，还有难以计数的技术内容

------

> 每 18 - 24 个月，前端开发就难一倍！
>
> 深JS
`
    },
    {
        title: '',
        background: './images/digg.png',
        content: ``
    },
    {
        title: '那又如何挖掘这些内容呢？',
        background: './images/how.png',
        content: ``
    },
    {
        title: '',
        background: './images/approach.png',
        content: ``
    },
    {
        title: '当然，还会有「 高玩 」',
        content: `高手总是用自定义的模式

![高手](./images/gaoshou.gif)
`
    },
    {
        title: 'Example: Angular.js',
        background: './images/progress.png',
        content: `
> 阅读 => 收藏  => 分享 => 审核
>
> 用户的行为转化为质量分层的依据`
    },
    {
        title: '一个互联网技术内容的图谱',
        background: './images/graph.png',
        content: `
> [Angular.js]
> 
> 关注你最感兴趣的技术分类
>
> [Google] [ECMAScript 6] [MVVM]
> 
> 通过你的行为，推荐最有用的内容
`
    },
    {
        title: '如果我现在再学习 LAMP',
        content: `
我会关注 [PHP] [MySQL] [网站开发] 等分类

------

基于我的阅读、收藏数据，我很快会去接触到

[Laravel] [PostgreSQL] [ORM] 等等相关的知识内容
`
    },
    {
        title: '想想这些信息未来会如何有效地排列，还有点小激动呢',
        background: './images/connection.png',
        content: ``
    },
    {
        title: '这就是「 掘金 」在做的事情',
        content: `
希望它可以早点变成完整体

![进化](./images/evolve.gif)

Thanks, Ming
        `
    }
]

import section from './components/section.vue'

export default {
    replace: false,
    data () {
        return {
            sections: sections,
            totalLength: sections.length
        }
    },
    components: {
        'section-view': section
    }
}

</script>