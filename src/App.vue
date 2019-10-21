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

@media screen and (max-width: 1250px) {
    #hero .hero-text .hero-desc {
        width:calc(100% - 600px)
    }

    .widget.widget--featured {
        padding: 50px 20px 0!important
    }

    .widget.widget--featured .widget-title {
        text-align: center
    }

    .widget.widget--featured .featured-list {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap
    }

    .widget.widget--featured .featured-list a {
        -ms-flex-preferred-size: calc(50% - 10px);
        flex-basis: calc(50% - 10px)
    }

    .widget.widget--featured .featured-list a:nth-child(2n) {
        margin-left: auto
    }

    .widget.widget--featured .featured-list .item {
        margin: 0 0 20px !important;
        border-radius: 10px;
        position: relative;
        background: #303030;
        display: block !important;
        width: 100%;
        height: 310px;
        -webkit-box-sizing: border-box;
        box-sizing: border-box;
        padding-top: 235px
    }

    .widget.widget--featured .featured-list .item .item-text {
        display: block !important;
        text-align: center !important;
        height: auto !important;
        border-radius: 0 0 10px 10px !important;
        padding: 0 !important;
    }

    .widget.widget--featured .featured-list .item .item-text .item-title {
        margin-top: 0 !important;
    }

    .widget.widget--featured .featured-list .item .item-text .white-line:after {
        display: none
    }

    .widget.widget--featured .featured-list .item .item-img {
        float: none !important;
        margin: 0 !important;
        width: calc(100% - 40px) !important;
        display: block !important;
        height: 190px !important;
        position: absolute !important;
        top: 20px !important;
        left: 20px !important;
    }
}

@media screen and (max-width: 1100px) {
    #hero {
        margin-bottom:20px
    }

    #hero .hero-img {
        bottom: -5px;
        right: 30px
    }

    .row .sidebar {
        -ms-flex-preferred-size: 35%;
        flex-basis: 35%
    }

    .row .sidebar .widget:not(:last-of-type) {
        margin-bottom: 20px
    }

    .row .main {
        -ms-flex-preferred-size: calc(65% - 20px);
        flex-basis: calc(65% - 20px)
    }

    .widget--latest .latest-img {
        bottom: -5px
    }
}

@media screen and (max-width: 1020px) {
    #hero .hero-text .hero-desc {
        width:auto !important;
        position: relative !important;
        bottom: auto !important;
        left: auto !important;
        margin-top: 20px !important;
        text-align: justify !important;
        display: block !important;
    }

    #hero .widget {
        min-height: 0
    }

    #hero .hero-img {
        width: 300px;
        height: 200px;
        margin-top: 25px;
        top: 0;
        right: 25px;
        height: calc(100% - 48px)
    }

    #hero .hero-img:after,#hero .hero-img:before {
        display: none
    }

    #hero .widget-home-ad .hero-title {
        font-size: 24px;
        text-align: left!important
    }

    #hero .widget-home-ad .hero-title:after {
        width: 30px
    }
}

@media screen and (min-width: 800px) and (max-width:1002px) {
    .sidebar {
        display:-webkit-box;
        display: -ms-flexbox;
        display: flex;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap
    }

    .sidebar>.widget {
        width: calc(50% - 10px)!important;
        display: inline-block!important;
        vertical-align: top
    }

    .sidebar>.widget:nth-child(2n) {
        margin-left: auto!important
    }
}

@media screen and (max-width: 1002px) {
    #hero {
        margin-bottom:0
    }

    #hero .hero-text,#hero .hero-text .hero-title {
        display: block;
        text-align: center
    }

    #hero .hero-subtitle {
        text-align: center
    }

    .row {
        display: block!important
    }

    .widget {
        padding: 50px!important;
        width: 100%!important;
        max-width: none!important;
        display: block!important;
        margin: 0 0 20px!important
    }

    footer {
        margin-top: 0
    }

    .widget.widget--latest .latest-img {
        position: relative !important;
        bottom: -20px !important;
        max-width: 100%
    }
}

@media (max-width: 725px) {
    .widget.widget--about .about-text {
        font-size:13px
    }

    .widget.widget--featured .featured-list {
        padding-bottom: 1px;
        display: block
    }

    #hero .widget.widget-home-ad {
        padding-top: 285px !important
    }

    #hero .widget.widget-home-ad .hero-text {
        width: 100% !important;
    }

    #hero .widget.widget-home-ad .hero-text .white-line:after {
        display: none
    }

    #hero .widget.widget-home-ad .hero-text .hero-title {
        text-align: center!important
    }

    #hero .widget.widget-home-ad .hero-img {
        right: auto;
        margin: 0;
        width: calc(100% - 50px);
        height: 200px;
        top: 25px;
        left: 25px;
    }
}

@media (max-width: 450px) {
    .widget.widget--about {
        padding:30px!important
    }

    .widget.widget--about .widget-title {
        margin-top: 10px;
        margin-bottom: 30px
    }

    .widget.widget--latest {
        padding-left: 25px!important;
        padding-right: 25px!important;
        padding-bottom: 45px!important
    }
}

@media (max-width: 350px) {
    #hero .widget.widget-home-ad {
        padding:255px 25px 25px!important
    }
}

@media (max-width: 1000px) {
    .widget.widget--footer {
        margin-bottom:55px!important
    }

    .widget.widget--footer ul {
        top: 41px
    }

    footer .container>span {
        display: block;
        text-align: center
    }
}

@media (max-width: 650px) {
    .widget.widget--footer:after,.widget.widget--footer:before {
        top:auto;
        height: 50%;
        bottom: calc(100% - 175px);
        -webkit-transform: rotate(-3deg);
        -ms-transform: rotate(-3deg);
        transform: rotate(-3deg);
        right: 0;
        left: -20px;
        width: 120%
    }

    .widget.widget--footer:after {
        bottom: calc(100% - 165px);
        -webkit-transform: rotate(3deg);
        -ms-transform: rotate(3deg);
        transform: rotate(3deg)
    }

    .widget.widget--footer h3 {
        text-align: center;
        display: block;
        margin-bottom: 70px
    }

    .widget.widget--footer ul {
        position: relative;
        right: 0
    }

    .widget.widget--footer ul li {
        margin-bottom: 30px;
        text-align: center
    }

    .widget.widget--footer ul li a:before {
        display: block;
        float: none;
        margin: 0 auto 4px
    }
}

@media (max-width: 1002px) {
    #portfolio .portfolio-holder {
        margin:0 0 70px
    }

    #portfolio .portfolio-holder .item.widget {
        padding: 30px!important;
        width: calc(50% - 10px)!important;
        margin: 0 5px 10px!important
    }

    #portfolio .portfolio-holder .item.widget .item-img-box img {
        min-width: 100%;
        max-height: 100%;
        width: auto;
        height: auto
    }
}

@media (max-width: 540px) {
    #portfolio .portfolio-holder .item.widget {
        width:100%!important;
        margin: 0 10px!important
    }

    #portfolio .portfolio-holder .item.widget .item-img-box img {
        max-height: none;
        min-width: none;
        width: 100%
    }
}

@media (max-width: 450px) {
    #portfolio .portfolio-holder .item.widget .item-img-box img {
        height:100%;
        width: auto
    }
}

@media (max-width: 1002px) {
    #hero .row .widget.widget--hero_skills .skill-group {
        margin-bottom:30px
    }

    #hero .row .widget.widget--hero_skills .skill-group:last-child {
        margin-bottom: 0
    }

    #hero .row .widget.widget--hero_skills .skill-group .skill-list .skill {
        width: calc(33.333% - 10px);
        height: 44px
    }

    #hero .row .widget.widget--hero_skills .skill-group .skill-stars {
        left: 0;
        right: 0;
        margin: auto
    }
}

@media (max-width: 650px) {
    #hero .row .widget.widget--hero_skills .skill-group:not(:last-child) {
        margin-bottom:50px
    }

    #hero .row .widget.widget--hero_skills .skill-group .skill-list .skill {
        display: block;
        width: auto;
        margin-bottom: 10px
    }
}

@media (max-width: 1002px) and (min-width:650px) {
    .sidebar .widget.widget--about {
        width:100%!important
    }

    .sidebar .widget.widget--about .about-text {
        text-align: center;
        line-height: 26px;
        font-size: 14px
    }
}
</style>
