<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
a,abbr,acronym,address,applet,article,aside,audio,b,big,blockquote,
body,canvas,caption,center,cite,code,dd,del,details,dfn,div,dl,dt,
em,embed,fieldset,figcaption,figure,footer,form,h1,h2,h3,h4,h5,h6,
header,hgroup,html,i,iframe,img,ins,kbd,label,legend,li,mark,menu,
nav,object,ol,output,p,pre,q,ruby,s,samp,section,small,span,strike,
strong,sub,summary,sup,table,tbody,td,tfoot,th,thead,time,tr,tt,u,
ul,var,video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline
}

article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section {
    display: block
}

body {
  font-family: 'Roboto', sans-serif;
  color: white;
  background: #232323;
  line-height: 1;
  margin: 0;
}

ol,ul {
    list-style: none
}

blockquote,q {
    quotes: none
}

blockquote:after,blockquote:before,q:after,q:before {
    content: '';
    content: none
}

table {
    border-collapse: collapse;
    border-spacing: 0
}

a {
  text-decoration: none
}

.container {
  width: 1310px;
  max-width: 100%;
  padding: 0 20px;
  margin: 0 auto;
  -webkit-box-sizing: border-box;
  box-sizing: border-box
}

.widget {
    background-color: #373737;
    border-radius: 10px;
    padding: 70px;
    cursor: default;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    position: relative;
    display: block;
    -webkit-box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s
}

.widget .widget-title {
    font-size: 28px;
    line-height: 36px;
    display: block;
    margin-bottom: 40px;
    font-weight: bold
}

.sidebar .widget .widget-title {
    text-align: center
}

.widget.link {
    display: block;
    cursor: pointer;
    -webkit-transition: .3s;
    -o-transition: .3s;
    transition: .3s;
    color: white
}

.widget.link:hover {
    -webkit-transform: scale(0.99);
    -ms-transform: scale(0.99);
    transform: scale(0.99)
}

.widget.wave {
    background: #373737 url(/web/20190118210241im_/http://beta.nikolovdzn.com/static/img/wave.svg) no-repeat bottom center/105% auto
}

.widget.wave:hover {
    background-size: 1550px auto
}

.row {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: stretch;
  -ms-flex-align: stretch;
  align-items: stretch;
  -ms-flex-wrap: nowrap;
  flex-wrap: nowrap
}

.row .sidebar {
  -webkit-transition: .25s;
  -o-transition: .25s;
  transition: .25s;
  -ms-flex-preferred-size: 30%;
  flex-basis: 30%
}

.row .sidebar .widget:not(:last-of-type) {
  margin-bottom: 50px
}

.row .main {
  -webkit-transition: .25s;
  -o-transition: .25s;
  transition: .25s;
  -ms-flex-preferred-size: calc(70% - 50px);
  flex-basis: calc(70% - 50px);
  margin-left: auto
}

.white-line:after {
  content: "";
  display: block;
  width: 65px;
  height: 5px;
  background: white;
  border-radius: 6px;
  margin: 30px 0 0;
  position: relative;
  left: 0;
  -webkit-transition: .25s;
  -o-transition: .25s;
  transition: .25s
}
</style>
