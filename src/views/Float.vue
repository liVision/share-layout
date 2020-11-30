/* 文字围绕浮动元素排版，但我们可能希望文字（.textDiv）排列在浮动元素下方，或者，我们并不希望.textDiv两边有浮动元素存在。
浮动元素排版超出了其父级元素（.topDiv），父元素的高度出现了塌缩，若没有文字高度的支撑，不考虑边框，父级元素高度会塌缩成零。
浮动元素甚至影响到了其父元素的兄弟元素（.bottomDiv）排版。因为浮动元素脱离了文档流，.bottomDiv在计算元素位置的时候会忽略其影响，紧接着上一个元素的位置继续排列 */
<template>
    <div>
        <div class="topDiv">
            <div class="floatDiv">float left</div>
            <div class="textDiv">你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。</div>
            <div class="blankDiv"></div>
        </div>
        <div class="bottomDiv">你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。你们看我的位置，围绕浮动元素。</div>
    </div>
</template>

<style lang="scss" scoped>
    .topDiv {
        width: 500px;
        border: 2px solid black;
    }
    .floatDiv {
        width: 100px;
        height: 100px;
        border: 2px dotted red;
        color: red;
        margin: 4px;
        float: left;
    }
    .bottomDiv {
        width: 500px;
        height: 100px;
        margin: 5px 0;
        border: 2px dotted black;
    }
    .textDiv {
        color: blue;
        border: 2px solid blue;
    }




    /* 利用clear清除浮动 */
    /* .topDiv {
        width: 500px;
        border: 2px solid black;
    }
    .floatDiv {
        width: 100px;
        height: 100px;
        border: 2px dotted red;
        color: red;
        margin: 4px;
        float: left;
    }
    .bottomDiv {
        width: 500px;
        height: 100px;
        margin: 5px 0;
        border: 2px dotted black;
    }
    .textDiv {
        color: blue;
        border: 2px solid blue;
    }
    // 区别在这里
    .blankDiv {
        clear: both; // or left
    } */


    // 利用overflow清除浮动
    /* .topDiv {
        overflow: auto;
        zoom: 1;  
        width: 500px;
        border: 2px solid black;
    }
    .floatDiv {
        width: 100px;
        height: 100px;
        border: 2px dotted red;
        color: red;
        margin: 4px;
        float: left;
    }
    .bottomDiv {
        width: 500px;
        height: 100px;
        margin: 5px 0;
        border: 2px dotted black;
    }
    .textDiv {
        color: blue;
        border: 2px solid blue;
    } */


    // 通过伪类清除浮动
    .topDiv {
        zoom: 1; 
        width: 500px;
        border: 2px solid black;
    }
    .topDiv:after {
        content: "";
        display: block;
        height: 0;
        visibility: hidden;
        clear: both;
    }
    .floatDiv {
        width: 100px;
        height: 100px;
        border: 2px dotted red;
        color: red;
        margin: 4px;
        float: left;
    }
    .bottomDiv {
        width: 500px;
        height: 100px;
        margin: 5px 0;
        border: 2px dotted black;
    }
    .textDiv {
        color: blue;
        border: 2px solid blue;
    }

</style>