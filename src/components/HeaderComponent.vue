<template>
  <header>
    <nav class="container">
      <a id="logo" href="/">
        <b>Header</b>Text
      </a>
      <ul class="nav-links">
        <li class="portfolio">
          <a href="/portfolio">
            Portfolio
          </a>
        </li>
        <li class="services">
          <a href="/services">
            Services
          </a>
        </li>
        <li class="contact">
          <a href="/contact">
            Contact
          </a>
        </li>
        <li class="blog">
          <a href="/blog">
            Blog
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header {
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s;
    position: relative;
    overflow: hidden;
    width: 100%;
    height: 400px
}

header:before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    -webkit-clip-path: polygon(0 0, 100% 0, 100% 88%, 0 100%);
    clip-path: polygon(0 0, 100% 0, 100% 88%, 0 100%);
    background: #3498db;
    background: -moz-linear-gradient(top, #3498db 0%, #2980b9 100%);
    background: -webkit-gradient(linear, left top, left bottom,
      color-stop(0%, #3498db), color-stop(100%, #2980b9));
    background: -webkit-linear-gradient(top, #3498db 0%, #2980b9 100%);
    background: -o-linear-gradient(top, #3498db 0%, #2980b9 100%);
    background: -ms-linear-gradient(top, #3498db 0%, #2980b9 100%);
    background: -webkit-gradient(linear, left top, left bottom, from(#3498db), to(#2980b9));
    background: linear-gradient(to bottom, #3498db 0%, #2980b9 100%);
    filter: progid:DXImageTransform.Microsoft.gradient(
      startColorstr='#ffffff', endColorstr='#000000',GradientType=0 )
}

header nav {
    font-size: 0;
    height: 150px;
    line-height: 158px
}

header nav #logo {
    float: left;
    display: inline-block;
    text-transform: uppercase;
    color: white;
    font-size: 16px;
    letter-spacing: 5px;
    position: relative;
    text-shadow: 0 3px 1px rgba(0, 0, 0, 0.2);
}

header nav #logo:before {
    content: "";
    display: inline-block;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    margin-right: 20px;
    margin-top: 4px;
    height: 150px;
    float: left;
    width: 20px;
    background: url("/images/logo.png") no-repeat center/100% auto;
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s;
    opacity: .5
}

header nav #logo b {
    padding-left: 20px;
    border-left: 1px solid rgba(255, 255, 255, 0.15);
    font-weight: bold
}

header nav #logo:hover:before {
    opacity: 1
}

header nav ul {
    float: right;
    display: inline-block;
    position: relative
}

header nav ul li {
    display: inline-block
}

header nav ul li a {
    opacity: .75;
    display: inline-block;
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s;
    color: white;
    font-weight: bold;
    position: relative;
    font-size: 18px;
    margin-left: 40px
}

header nav ul li a:hover {
    opacity: 1
}

header nav ul li a:before {
    display: inline-block;
    margin-bottom: -5px;
    margin-right: 15px;
    width: 25px;
    height: 25px;
    mask: no-repeat center;
    -webkit-mask: no-repeat center
}

header nav ul li a.active {
    color: #E8CD9C;
    opacity: 1
}

header nav ul li a.active:before {
    background-color: #E8CD9C
}

header nav ul li a.active:after {
    position: absolute;
    bottom: 50px;
    right: 0;
    border-radius: 10px;
    width: 25%;
    height: 4px;
    background: rgba(255, 255, 255, 0.25);
    display: block
}

header nav ul li.portfolio a:before {
  font-family: "Font Awesome 5 Free";
  content: "\f518";
}

header nav ul li.services a:before {
  font-family: "Font Awesome 5 Free";
  content: "\f0e7";
}

header nav ul li.contact a:before {
  font-family: "Font Awesome 5 Free";
  content: "\f086";
}

header nav ul li.blog a:before {
  font-family: "Font Awesome 5 Free";
  content: "\f022";
}

@media screen and (max-width: 900px) {
    header {
        height:440px
    }

    header nav.container {
        padding-top: 30px;
        height: 70px;
        line-height: 70px
    }

    header nav.container #logo {
        float: none;
        text-align: center;
        display: table;
        margin: 0 auto
    }

    header nav.container #logo:before {
        height: 70px;
        margin-top: 0
    }

    header nav.container ul {
        float: none;
        display: block;
        text-align: center
    }

    header nav.container ul li a.active:after {
        bottom: 6px
    }
}

@media screen and (max-width: 600px) {
    header {
        height:450px
    }

    header nav.container ul {
        padding-top: 19px
    }

    header nav ul li:first-child a {
        margin-left: 0
    }

    header nav ul li a {
        text-align: center;
        font-size: 14px
    }

    header nav ul li a.active:after {
        margin: 0 auto;
        left: 0;
        bottom: 8px!important
    }

    header nav ul li a:before {
        display: block;
        float: none;
        margin: 0 auto 0px
    }
}

@media screen and (max-width: 350px) {
    header {
        height:444px
    }

    header nav.container #logo {
        font-size: 0;
        text-align: center;
        height: 70px;
        display: block;
        line-height: 70px
    }

    header nav.container #logo:before {
        padding: 0;
        margin: 0 auto;
        float: none;
        display: block
    }

    header nav ul li a {
        line-height: 25px;
        font-size: 0
    }

    header nav ul li a:after {
        display: none!important
    }
}
</style>
