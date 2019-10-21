<template>
  <div>
    <HeaderComponent/>
    <div id="content" class="container">
      <div id="hero">
        <div class="widget widget-home-ad link">
          <div class="gradient"/>
          <div class="hero-text stick-left">
            <h3 class="hero-title white-line">
              Hero heading text
            </h3>
            <span class="hero-desc">
              Hero description text.
            </span>
          </div>
          <div class="hero-img"/>
        </div>
      </div>
      <div class="row">
        <div class="sidebar">
          <div class="widget widget--about">
            <h3 class="widget-title">Hello!</h3>
            <span class="about-text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit,
              sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
              Ut enim ad minim veniam, quis nostrud exercitation ullamco
              laboris nisi ut aliquip ex ea commodo consequat.
              Duis aute irure dolor in reprehenderit in voluptate velit
              esse cillum dolore eu fugiat nulla pariatur.
              Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
              officia deserunt mollit anim id est laborum.
              <br><br>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit,
              sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
              Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat.
              Duis aute irure dolor in reprehenderit in voluptate velit esse
              cillum dolore eu fugiat nulla pariatur.
              Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
              officia deserunt mollit anim id est laborum.
            </span>
          </div>
          <a href="/" target="_blank" class="widget wave link widget--latest">
          <h3 class="widget-title">Latest</h3>
          <span class="latest-details">
            <b>Project Name</b>
            Project Description
          </span>
          <div class="latest-img"/>
          </a>
        </div>
        <div class="main">
          <div class="widget widget--featured">
            <h3 class="widget-title">Featured Work</h3>
            <ul class="featured-list">
              <a href="/" target="_blank">
                <li class="item">
                  <div class="item-text">
                    <h3 class="item-title">Project Name</h3>
                    <span class="item-tags white-line">Project Description</span>
                  </div>
                  <div class="item-img" style="background-image:url(/images/logo.png)"></div>
                </li>
              </a>
              <a href="/" target="_blank">
                <li class="item">
                  <div class="item-text">
                    <h3 class="item-title">Project Name</h3>
                    <span class="item-tags white-line">Project Description</span>
                  </div>
                  <div class="item-img" style="background-image:url(/images/logo.png)"></div>
                </li>
              </a>
              <a href="/" target="_blank">
                <li class="item">
                  <div class="item-text">
                    <h3 class="item-title">Project Name</h3>
                    <span class="item-tags white-line">Project Description</span>
                  </div>
                  <div class="item-img" style="background-image:url(/images/logo.png)"></div>
                </li>
              </a>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <FooterComponent/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderComponent from '@/components/HeaderComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  name: 'home',
  components: {
    HeaderComponent,
    FooterComponent,
  },
};
</script>

<style scoped lang="scss">
#hero {
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s;
    margin-top: -250px;
    margin-bottom: 50px
}

#hero .row {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: stretch;
    -ms-flex-align: stretch;
    align-items: stretch
}

#hero .row .widget {
    -webkit-box-flex: 1!important;
    -ms-flex: 1!important;
    flex: 1!important;
    -ms-flex-positive: 1;
    flex-grow: 1
}

#hero .row .widget.smaller {
    padding: 50px;
    max-width: calc(40% - 50px);
    margin: 0 auto
}

#hero .row .widget.smaller:first-child {
    margin-right: 50px
}

#hero .row .widget.smaller:last-child {
    margin-left: 50px
}

@media (max-width: 1100px) {
    #hero .row .widget.smaller:last-child {
        margin-left:20px
    }
}

#hero .hero-subtitle {
    font-size: 12px;
    font-weight: bold;
    color: #fff;
    margin: 4px 0 30px;
    display: block
}

#hero .widget {
    position: relative;
    min-height: 345px;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    background:#3498db
}

#hero .gradient {
    display: block;
    position: absolute;
    z-index: 0;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%
}

#hero .gradient:after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 50%;
    opacity: 0;
    -webkit-transition: .5s;
    -o-transition: .5s;
    transition: .5s;
    background: transparent;
    background: -moz-linear-gradient(top, transparent 0%, #2980b9 100%);
    background: -webkit-gradient(linear, left top, left bottom, color-stop(0%, transparent),
      color-stop(100%, #2980b9));
    background: -webkit-linear-gradient(top, transparent 0%, #2980b9 100%);
    background: -o-linear-gradient(top, transparent 0%, #2980b9 100%);
    background: -ms-linear-gradient(top, transparent 0%, #2980b9 100%);
    background: -webkit-gradient(linear, left top, left bottom, from(transparent), to(#2980b9));
    background: linear-gradient(to bottom, transparent 0%, #2980b9 100%);
    filter: progid:DXImageTransform.Microsoft.gradient(
      startColorstr='#ffffff', endColorstr='#000000',GradientType=0 );
    border-radius: 8px
}

#hero .widget.link:hover .gradient:after {
    opacity: 1;
    height: 100%
}

#hero .widget.link:hover .hero-title:after {
    width: 6px;
    border-radius: 100%;
    left: calc(100% - 5px)
}

#hero .widget.text-center {
    text-align: center
}

#hero .widget.text-center .hero-title {
    margin: 0 auto
}

#hero .hero-text {
    display: inline-block
}

#hero .hero-text.stick-left {
    height: 100%;
    width: 50%
}

#hero .hero-text .hero-title {
    display: table;
    font-size: 30px;
    font-weight: bold
}

#hero .hero-text .hero-title.mini {
    max-width: 300px;
    line-height: 30px;
    font-size: 26px
}

#hero .hero-text .hero-desc {
    position: absolute;
    color: #fff;
    bottom: 60px;
    left: 70px;
    width: calc(100% - 750px)
}

#hero .hero-text .hero-desc b {
    font-weight: bold;
    color: #fff
}

#hero .hero-text .hero-paragraph {
    color: #fff;
    font-size: 13px;
    line-height: 20px;
    margin-top: 10px;
    text-align: justify
}

#hero .hero-text .hero-paragraph b {
    font-weight: bold;
    color: #fff
}

#hero .hero-text .hero-paragraph:first-of-type {
    margin-top: 40px
}

#hero .hero-img {
    background: #444;
    border-radius: 10px;
    position: absolute;
    bottom: -15px;
    right: 55px;
    display: block;
    width: 440px;
    height: 265px;
    -webkit-box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s
}

#hero .hero-img:after,#hero .hero-img:before {
    content: "";
    display: block;
    position: absolute;
    width: 90%;
    left: 5%;
    border-radius: 10px 10px 0 0;
    top: -12px;
    height: 12px;
    background: rgba(0, 0, 0, 0.075)
}

#hero .hero-img:after {
    top: -24px;
    background: rgba(0, 0, 0, 0.025);
    width: 80%;
    left: 10%
}

.widget--latest {
    margin-top: 50px;
    padding-bottom: 245px;
    -webkit-transition: .5s;
    -o-transition: .5s;
    transition: .5s
}

@media (max-width: 1100px) {
    .widget--latest {
        margin-top:20px
    }
}

.widget--featured {
    padding-bottom: 0
}

.widget--featured a {
    color: white
}

.widget--featured .featured-list {
    text-align: right
}

.widget--featured .featured-list .item {
    display: inline-block;
    margin-right: -85px;
    margin-bottom: 50px
}

.widget--featured .featured-list .item .item-text {
    vertical-align: text-bottom;
    display: inline-block;
    text-align: right;
    height: 238px;
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s
}

.widget--featured .featured-list .item .item-text .item-title {
    margin-top: 118px;
    color: #3498db;
    line-height: 28px;
    font-size: 22px;
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s;
    font-weight: bold
}

.widget--featured .featured-list .item .item-text .item-tags {
    font-weight: bold;
    color: #777;
    font-size: 12px
}

.widget--featured .featured-list .item .item-text .item-tags:after {
    width: 52px;
    margin-left: auto
}

.widget--featured .featured-list .item .item-img {
    width: 390px;
    height: 238px;
    background: #ccc no-repeat center / cover;
    float: right;
    margin-left: 50px;
    display: inline-block;
    border-radius: 10px;
    -webkit-box-shadow: -5px 5px 20px rgba(0, 0, 0, 0.15);
    box-shadow: -5px 5px 20px rgba(0, 0, 0, 0.15);
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s
}

.widget--featured .featured-list .item:hover .item-text .item-title {
    color: white
}

.widget--featured .featured-list .item:hover .item-text .item-tags:after {
    width: 4px;
    border-radius: 50%
}

.widget--featured .featured-list .item:hover .item-img {
    margin-left: 30px;
    border-radius: 20px
}


.widget--latest:after {
    content: "\f35a";
    font-family: "Font Awesome 5 Free";
    font-size: 22px;
    position: absolute;
    color: rgba(255, 255, 255, 0.75);
    opacity: 0;
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s;
    top: 25px;
    right: 25px
}

.widget--latest:hover:after {
    opacity: 1
}

.widget--latest:hover .latest-details {
    color: white
}

.widget--latest .latest-details {
    display: block;
    text-align: center;
    font-size: 11px;
    color: #999;
    margin: 50px 0 10px;
    line-height: 20px;
    -webkit-transition: color .25s;
    -o-transition: color .25s;
    transition: color .25s
}

.widget--latest .latest-details b {
    font-size: 16px;
    color: #fff;
    font-weight: bold;
    display: block
}

.widget--latest .latest-img {
    position: absolute;
    bottom: -15px;
    left: 0;
    right: 0;
    margin: auto;
    width: 289px;
    height: 220px;
    background: #999 no-repeat center / cover;
    border-radius: 10px
}


.widget.wave {
    background: #373737 url(/images/wave.svg) no-repeat bottom center/105% auto
}

.widget.wave:hover {
    background-size: 1550px auto
}

</style>
