<template>
  <footer>
    <div class="container">
      <div class="widget widget--footer">
        <h3><small>Footer text goes in here.</small> And Here</h3>
        <ul>
          <li><a class="skype" href="#">skype_link</a></li>
          <li><a class="discord" href="#">discord_link</a></li>
          <li><a class="email" href="#">email_link</a></li>
        </ul>
      </div>
      <span>Copyright BoostLab © 2019. All Rights Reserved.</span>
      <a id="backTop"></a>
    </div>
  </footer>
</template>

<script>

</script>

<style scoped lang="scss">
footer {
    overflow: hidden;
    margin-top: 50px;
    cursor: default;
    position: relative
}

footer:after,footer:before {
    content: "";
    position: absolute;
    top: 40%;
    left: -25%;
    width: 150%;
    height: 150%;
    background: #0E0E0E;
    -webkit-transform: rotate(-2deg);
    -ms-transform: rotate(-2deg);
    transform: rotate(-2deg)
}

footer:before {
    top: 30%;
    -webkit-transform: rotate(-1deg);
    -ms-transform: rotate(-1deg);
    transform: rotate(-1deg);
    background: #1E1E1E;
}

footer span {
    position: relative;
    color: #444;
    font-weight: bold
}

footer .container {
    z-index: 1;
    position: relative;
    padding-bottom: 50px
}

.widget--footer {
    background: #1A1A1A;
    color: #3498db;
    font-weight: bold;
    -webkit-box-shadow: 0 10px 10px rgba(0, 0, 0, 0.15);
    box-shadow: 0 10px 10px rgba(0, 0, 0, 0.15);
    margin-bottom: 50px;
    overflow: hidden
}

.widget--footer:after,.widget--footer:before {
    content: "";
    position: absolute;
    top: -50px;
    right: -20px;
    width: 400px;
    height: 150%;
    -webkit-transform: rotate(10deg);
    -ms-transform: rotate(10deg);
    transform: rotate(10deg);
    background: #1F1E1E
}

.widget--footer:before {
    right: 20px;
    background: #1D1B1B
}

.widget--footer h3 {
    display: inline-block;
    font-size: 30px;
    margin-top: 6px;
    position: relative;
    z-index: 1
}

.widget--footer h3 small {
    display: block;
    font-size: 14px;
    margin-bottom: 4px
}

.widget--footer ul {
    display: block;
    position: absolute;
    z-index: 1;
    top: 59px;
    right: 70px
}

.widget--footer ul>li>a {
    display: block;
    font-size: 13px;
    color: #3498db;
    margin: 0 0 14px;
    line-height: 20px;
    -webkit-transition: .25s;
    -o-transition: .25s;
    transition: .25s
}

.widget--footer ul>li>a:before {
    content: "";
    display: block;
    width: 18px;
    height: 20px;
    text-align: right;
    font-family: FontAwesome;
    font-size: 20px;
    line-height: 20px;
    float: left;
    margin-right: 15px
}

.widget--footer ul>li>a:hover {
    color: white
}

.widget--footer ul>li>a.skype:before {
  font-family: "Font Awesome 5 Brands";
  content: "\f17e";
}

.widget--footer ul>li>a.discord:before {
  font-family: "Font Awesome 5 Brands";
  content: "\f392";
}

.widget--footer ul>li>a.email:before {
  font-family: "Font Awesome 5 Free";
  content: "\f674";
}
</style>
