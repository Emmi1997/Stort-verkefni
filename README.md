# Stort-verkefni
Vefsíða

# Um.html

<!doctype html>
<html class="grid" lang="is">
  <head>
    <meta charset="utf-8">
    <title>Stort Verkefni 6 - Um</title>
    <link href="https://fonts.googleapis.com/css?family=Lato|Merriweather" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="grid.css">
  </head>
</head>
<body>
  <header class="header col-12">
    <section class="header__top_bar col-12">
      <p>Fooþjónusta</p>
      <nav class="header__nav">
        <a href="">Um</a>
        <button class="button">Kaupa</button>
      </nav>
    </section>
    <section class="header__image col-12 row col offset_wider">
    <heading class="heading col-6">
      <h1 class="heading--two">Um Fooþjónustuna</h1>
    </heading>
  </section>
  </header>
  <main>
    <section class="main_content">
      <h2 class="heading heading--three">Hvað er Fooþjónusta ?</h2>
      <p class="text text__p">
        Í hinum ódauðlegu orðum stofnanda okkar:
      </p>
      <p class="text text__p">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris varius
        lorem sit amet diam faucibus, et lacinia metus tempus. Nam vulputate
        erat non aliquet ultrices. Curabitur at ligula sit amet purus dictum
        tempor. Morbi ultrices suscipit mi vehicula viverra. Sed sit amet quam
        luctus tortor elementum iaculis. Sed pellentesque vel magna in
        condimentum. Pellentesque mollis, ante quis tristique rutrum, arcu
        elit fermentum enim, non rhoncus lacus lorem sagittis dolor.
        Suspendisse bibendum sapien rutrum lorem rutrum eleifend. Ut interdum
        feugiat magna, ac lacinia orci gravida eget. Ut egestas, nulla aliquam
        commodo gravida, enim nisl congue lectus, eu maximus tortor neque at
        velit. Praesent nec nunc purus. Duis lacus quam, aliquet et nulla sed,
        vestibulum interdum leo. Curabitur id ante et risus dictum maximus.
        Proin quis ligula tristique, hendrerit felis vel, ultrices tortor.
        Proin mattis lacus id aliquam maximus. Lorem ipsum dolor sit amet,
        consectetur adipiscing elit. Vestibulum vel metus risus.
      </p>
      <aside class="aside col-7">
        <blockquote class="blockquote">
          <p>„Aenean in purus vel leo pellentesque lacinia non ut magna.
          Sed eleifend tristique mollis.“</p>
          <p class="text text_p">— Foobarius Baz</p>
        </blockquote>
      </aside>
      <p class="text text__p">
        Donec efficitur ante scelerisque metus tempus aliquam. Etiam sit amet
        justo vulputate, ultricies ligula non, fringilla sapien. Mauris ut
        neque nec dui ullamcorper vulputate. Ut at suscipit est. Cras elementum
        tellus erat, quis dictum tellus efficitur quis. Sed mollis fermentum
        massa, hendrerit vehicula nunc hendrerit sit amet. Donec vestibulum
        tortor nec enim lobortis placerat. Quisque faucibus volutpat
        consectetur. Nunc sed ipsum egestas, semper massa non, consequat felis.
        Nam pellentesque sapien ipsum, et malesuada mi ultricies in. Donec
        consequat mattis consequat. Maecenas efficitur vehicula ultrices.
      </p>
      <p class="text text__p">
        Aenean in purus vel leo pellentesque lacinia non ut magna. Sed eleifend
        tristique mollis. Nam purus nisl, elementum eget vestibulum at,
        volutpat vitae diam. Proin vitae enim in elit condimentum fringilla.
        Quisque ullamcorper enim vel feugiat facilisis. Fusce commodo hendrerit
        ex. Donec posuere, enim non vehicula placerat, metus enim blandit nisi,
        eu rhoncus nisl mi et justo. Curabitur ullamcorper nec magna eu dictum.
        Maecenas tincidunt sem odio, nec blandit dolor ultricies eu.
        Donec viverra ipsum lobortis quam tincidunt lacinia. Aenean consectetur
        ut enim non lacinia. Proin sed interdum orci, et condimentum purus.
        Suspendisse vel erat sagittis, lobortis tortor vitae, pellentesque diam.
        Aenean fringilla elit id mi tincidunt tempus.
      </p>
    </section>
  </main>
  <footer class="footer row offset_wider">
    <div class="footer__higher_text_parent col-12">
      <div class="footer__higher_text--one">
        <p>Fooþjónustan</p>
        <p>123-4567</p>
      </div>
      <div class="footer__higher_text--two">
        <p>Opið 12-13 alla daga</p>
        <p>Bargata 1</p>
        <p>900 Foobar</p>
      </div>
    </div>
    <div class="footer__lower_text offset_thinner">
      <p class="text__p">
        © Fooþjónustan 2017
      </p>
    </div>
  </footer>
  </body>
</html>

# -------------------------------------------------------------
# Um.scss

// breytur fyrir mikið notaðar stærðir
$max-width: 1200px;
$gutter: 20px;

/* setjum box-sizing: border-box; á allt */
html { /* stylelint-disable-line */
  box-sizing: border-box;
}

*, *:before, *:after { /* stylelint-disable-line */
  box-sizing: inherit;

  /* fjarlægjum margin og padding */
  padding: 0;
  margin: 0;
}

html { /* stylelint-disable-line */
  // til þess að texti liggi ekki upp við brún á viewport þegar
  // við erum < 1200px breiðum skjá, setjum margin á báða kanta html
  // ruglar líka ekki í grid overlay
  margin-right: $gutter;
  margin-left: $gutter;

  font-family: Lato, helvetica, arial, sans-serif;
  font-size: 16px;
  line-height: 1.5;

  @media (min-width: $max-width) {
    margin: 0;
  }
}

body, main { /* stylelint-disable-line */
  max-width: $max-width;
  margin: 0 auto;

  // þar sem við erum að eiga við neikvæð margin á grid, setjum overflow-x
  // hér sem hidden, þá fáum við ekki lárétta skrunstiku
  overflow-x: hidden;
}

.main_content {
  margin-top: $gutter * 4;
  margin-bottom: $gutter * 4;
}

.aside{
  display: flex;
  margin-left: $gutter * 2;
  padding: ($gutter * 4) 0;
  float: right;
  height: 100%;
  justify-content: center;
}

.blockquote{
  padding-left: 11rem;
  padding-right: 1rem;
}

.blockquote p{
  padding-bottom: 1rem;
}

.footer{
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  height: $gutter * 10;
  background-color: #000;
  color: #eee;
  align-items: center;
  justify-content: space-around;

  &__higher_text_parent{
   display: flex;
   height: 50%;
   justify-content: center;
  }

  &__higher_text--one{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-right: $gutter * 5;
  }

  &__higher_text--two{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: $gutter * 4;
    margin-right: -($gutter / 2);
  }

  &__lower_text{
   color: #666;
   display: flex;
   flex-direction: row;
   justify-content: center;
   border-top: 2px solid #666;
  }
}

@import "scss/grid";
@import "scss/header";
@import "scss/heading";
@import "scss/text";
@import "scss/button";
@import "scss/card";
@import "scss/cardlist";

