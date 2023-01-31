# OHMYFOOD - Accommodations and Activities Website

### Author Links

👋 Hello, I'm Hordofel Dusty BAMANA.

👇 Follow Me:

- [Twitter](https://twitter.com/hordofel)
- [LinkedIn](https://www.linkedin.com/in/dusty-hordofel-bamana-08389310a)

---

### 🚀 Description

Ohmyfood! is a young startup that would like to impose itself on the restaurant market. The objective is to develop a 100% mobile site that lists the menus of gourmet restaurants. In addition to the classic reservation systems, customers will be able to compose the menu of their meal so that the dishes are ready when they arrive. No more waiting in restaurants! This is my third project from the application developer course - javascript react offered by [OpenClassRooms](https://openclassrooms.com/fr/paths/516-developpeur-dapplication-javascript-react) . Practice makes improvement.

---

## Section 1. Setup

---

### 1. Create folder structure

- create a github repository named `Ohmyfood`
- create index.html file.
- create sass folder with different folders in it.
- create images folder and put project images in it.
- create a setup branch `Setup` in github repository to save the setup folder structure
- add [legal notices](./mentions-legales/mentions-legales)

---

### 2. CSS styles

- compile sass folders and link css files with [index.html](index.html)
- import Roboto from Google Fonts in [main.scss](./sass/main.scss).
- link compiled [styles.css](./styles/styles.css) file to [html](index.html) file

```scss
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
</style>
font-family: 'Roboto', sans-serif;
```

- create color variables

```scss
$primary-color: #9356dc;
$secondary-color: #ff79da;
$tertiary-color: #99e2d0;
$Ohmyfood-white: #ffffff;
$Ohmyfood-primary-grey: #f7f7f7;
$Ohmyfood-secondary-grey: #eaeaea;
$Ohmyfood-shadow-1: 0 5px 15px rgba(0, 0, 0, 0.2);
$Ohmyfood-shadow-2: 0px 5px 6px 0px rgba(0, 0, 0, 0.2);
$Ohmyfood-shadow-3: 0 5px 15px rgba(0, 0, 0, 0.4);
$transition: all 0.3s linear;
$gradient: linear-gradient(
  180deg,
  rgba(255, 121, 218, 1) 0%,
  rgba(147, 86, 220, 1) 100%
);

// fontsize
$Ohmyfood-fs-1: 1.6rem;
$Ohmyfood-fs-2: 1.8rem;
$Ohmyfood-fs-3: 2.4rem;

//font weight
$Ohmyfood-fw-400: 400;
$Ohmyfood-fw-600: 600;
$Ohmyfood-fw-700: 700;
```

- create mixins

```scss
@mixin flexbox-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

@mixin button {
  opacity: 1;
  background: $gradient;
  color: white;
  border-radius: 200px;
  box-shadow: $Ohmyfood-shadow-1;
  font-size: $Ohmyfood-fs-1;
  padding: 20px;
  margin: 0 auto;
}

@mixin button-hover {
  opacity: 0.8;
  transition: 0.3s;
  box-shadow: $Ohmyfood-shadow-3;
}
```

- add global styles

```scss
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
  scroll-behavior: smooth;
}

body {
  font-family: "Roboto", sans-serif;
  background: $Ohmyfood-white;
  font-size: $Ohmyfood-fs-1;
}

a {
  text-decoration: none;
}

li {
  list-style: none;
}

img,
button,
a {
  display: block;
  text-decoration: none;
}

button {
  cursor: pointer;
  border: none;
}

span {
  display: inline-block;
}

input {
  display: block;
  width: 100%;
  font: inherit;
}
```

- use Font Awesome library

```css
<script src="https://kit.fontawesome.com/85893a34ce.js" crossorigin="anonymous"></script>
```

- add [Ohmyfood! favicon](./images/logo/favico/ohmyfoodfavicon.png)

- [create a pull request](https://github.com/Dusty-Hordofel/ohmyfood/pull/1)

---

## Section 2. Header

### 3. Header section

- add [header](./index.html)

```html
<!-- Logo -->
<header class="header">
  <a href="index.html">
    <img src="./images/logo/ohmyfood@2x.svg" alt="" class="header__logo" />
  </a>
</header>
<!-- end of Logo -->
```

- style [Header](./styles/styles.scss)

```scss
header {
  @include flexbox-center();
  width: 37.5rem;
  height: 6.4rem;
  background: yellow;
  box-shadow: $Ohmyfood-shadow-2;
}
```

## Section 3. Location

### 4. Location

- add [Location](./index.html)

```html
<!-- Localisation -->
<main class="main">
  <!-- location -->
  <div class="location">
    <div class="location__icon">
      <i class="fa-solid fa-location-dot"></i>
    </div>
    <div class="location__city">Paris, Belleville</div>
  </div>
  <!-- end of Location -->
</main>
```

- style [Location](./styles/styles.scss)

```scss
main {
  width: 37.5rem;

  .location {
    height: 4.9rem;
    background: $Ohmyfood-secondary-grey;
    @include flexbox-center();

    &__icon {
      width: 1.2rem;
      height: 1.6rem;
    }
    &__city {
      margin-left: 1.9rem; //à revoir en cas de changement d'écran
    }
  }
}
```

- create a [Location](https://github.com/Dusty-Hordofel/ohmyfood/pull/3) pull request

## Section 4. Main Section

### 5. Hero

- add [Hero](./index.html)

```html
<!-- Hero  section-->
<section class="hero">
  <div class="hero__container">
    <h1 class="hero__title">Réserver le menu qui vous convient</h1>
    <p class="hero__text">
      Découvrez des restaurants d'exception, sélectionnés par nos soins.
    </p>
    <button class="hero__button">Explorer nos restaurants</button>
  </div>
</section>
<!-- end of Hero  section-->
```

- style [Hero](./styles/styles.scss)

```scss
.hero {
  height: 28.6rem;
  background: $Ohmyfood-primary-grey;
  padding: 38px;
  &__title {
    margin: 0 30px 22px 30px;
  }

  &__text {
    margin-bottom: 34px;
  }
  &__button {
    @include button();
  }
}
```

### 6.Functioning

- add [Functioning-section](./index.html)

```html
<!-- Functioning section -->
<section class="functioning__container">
  <div class="functioning">
    <div class="functioning__title">
      <h2>Fonctionnement</h2>
    </div>
    <div class="functioning__buttons">
      <button class="functioning__button">
        <span class="functioning__button__number">1</span>
        <i
          class="fa-solid fa-mobile-screen-button functioning__button__icon"
        ></i>
        <p class="functioning__button__text">Choisissez un restaurant</p>
      </button>
      <button class="functioning__button">
        <span class="functioning__button__number">2</span>
        <i class="fa-solid fa-list functioning__button__icon"></i>
        <p class="functioning__button__text">Choisissez un restaurant</p>
      </button>
      <button class="functioning__button">
        <span class="functioning__button__number">3</span>
        <i class="fa-solid fa-store functioning__button__icon"></i>
        <p class="functioning__button__text">Choisissez un restaurant</p>
      </button>
    </div>
  </div>
</section>
<!-- end of Functioning section -->
```

- style [Functioning ](./styles/styles.scss)

```scss
/*----------functionning-section---------*/
.functioning__container {
  // background: #ff79da;
  // color: $Ohmyfood-black;
  height: 37.1rem;
  // height: 44.1rem;
  // padding-bottom: 70px;
  // margin-bottom: ;

  .functioning {
    &__title {
      color: $Ohmyfood-black;
      margin: 0px 0px 34px 25px;
    }

    &__buttons {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    &__button {
      position: relative;
      width: 32.5rem;
      height: 7.6rem;
      @include flexbox-center();
      background: #99e2d0;
      @include button(10px, $Ohmyfood-primary-grey, 20px);
      &:not(:nth-last-child(1)) {
        margin-bottom: 22px;
      }
      // margin-bottom: 22px;
      // padding: 70px;
      // @include button(20px, $Ohmyfood-primary-grey);
      &__number {
        position: absolute;
        left: -10px;
        background: $primary-color;
        border-radius: 50%;
        margin-right: 2.2rem;
        width: 2.5rem;
        height: 2.5rem;
        @include flexbox-center();
      }
      &__icon {
        color: $primary-color;
      }

      &__text {
        margin-left: 26px;
        display: inline-block;
        color: $Ohmyfood-black;
      }
    }
  }
}
```

### 7. Restaurants

- add [header](./index.html)

```html
<!-- Restaurant section -->
<section class="restaurant__container">
  <div class="restaurant">
    <div class="restaurant__title">
      <h2>Restaurants</h2>
    </div>
    <ul class="restaurant__menus">
      <li class="restaurant__menu">
        <div class="restaurant__menu__image">
          <img src="./images/restaurants/restaurant1.jpg" alt="" />
        </div>
        <div class="restaurant__menu__description">
          <div class="restaurant__menu__description__text">
            <h3>La palette du gout</h3>
            <p>Ménilmontant</p>
          </div>
          <div class="restaurant__menu__description__container">
            <i class="fas fa-heart restaurant__menu__description__icon"></i>
          </div>
        </div>
      </li>
      <li class="restaurant__menu">
        <div class="restaurant__menu__image">
          <img src="./images/restaurants/restaurant2.jpg" alt="" />
        </div>
        <div class="restaurant__menu__description">
          <div class="restaurant__menu__description__text">
            <h3>À la française</h3>
            <p>Cité Rouge</p>
          </div>
          <div class="restaurant__menu__description__container">
            <i class="fas fa-heart restaurant__menu__description__icon"></i>
          </div>
        </div>
      </li>
      <li class="restaurant__menu">
        <div class="restaurant__menu__image">
          <img src="./images/restaurants/restaurant3.jpg" alt="" />
        </div>
        <div class="restaurant__menu__description">
          <div class="restaurant__menu__description__text">
            <h3>Le délice des sens</h3>
            <p>Folie-Méricourt</p>
          </div>
          <div class="restaurant__menu__description__container">
            <i class="fas fa-heart restaurant__menu__description__icon"></i>
          </div>
        </div>
      </li>
      <li class="restaurant__menu">
        <div class="restaurant__menu__image">
          <img src="./images/restaurants/restaurant1.jpg" alt="" />
        </div>
        <div class="restaurant__menu__description">
          <div class="restaurant__menu__description__text">
            <h3>La palette du gout</h3>
            <p>Ménilmontant</p>
          </div>
          <div class="restaurant__menu__description__container">
            <i class="fas fa-heart restaurant__menu__description__icon"></i>
          </div>
        </div>
      </li>
    </ul>
  </div>
</section>
<!-- end of Restaurant section -->
```

- style [restaurants](./styles/styles.scss)

```scss
/*----------restaurants-section---------*/
.restaurant__container {
  height: 1121px;
  background: #99e2d0;
  margin-bottom: 65px;

  .restaurant {
    &__title {
      margin-left: 25px;
      background: #ff79da;
      margin-bottom: 20px;
    }

    &__menus {
      display: grid;
      background: #9356dc;
      justify-content: center;
      grid-column: 1fr;
      margin: 0 auto;
      gap: 20px;
    }

    &__menu {
      width: 343px;
      height: 253px;
      background: $Ohmyfood-white;
      border-radius: 20px;
      box-shadow: $Ohmyfood-shadow-1;
      &__image {
        img {
          height: 178px;
          width: 343px;
          object-fit: cover;
          border-radius: 20px 20px 0 0;
        }
      }

      &__description {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 25px;
        height: 75px;
        &__text {
        }
        &__icon {
          font-size: 25px;

          cursor: grab;
          &:hover {
            background: red;
          }
        }
      }
    }
  }
}
```

### 8. Footer

- add [footer](./index.html)

```html
<!-- Footer -->
    <footer class="footer__container">
      <div class="footer">
        <div class="footer__logo">
          <a href="index.html">
            <img src="./images/logo/ohmyfood@2x.svg" alt="" class="footer__logo_image" />
          </a>
        </div>
        <ul class="footer__links">
          <li class="footer__link">
            <a href="#" class="footer__link__info">
              <span>
                <i class="fa-solid fa-utensils"></i>
              </span>
              <p>
                Proposer un restaurant
              </p>
            </a>
          </li>
          <li class="footer__link">
            <a href="#" class="footer__link__info">
              <span>
                <i class="fa-solid fa-handshake-angle"></i>
              </span>
              <p>
                Devenir partenaire
              </p>
            </a>
          </li>
          <li class="footer__link">
            <a href="#" class="footer__link__info"> Mentions légales</a>
          </li>
          <li class="footer__link">
            <a href="#" class="footer__link__info"> Contact</a>
          </li>
        </ul>
      </div>
    </div>
    </footer>
```

- style [footer](./styles/styles.scss)

```scss
/****************footer****************/
footer {
  max-width: 37.5rem;
  height: 19.8rem;
  background: #353535;
  color: $Ohmyfood-white;

  .footer {
    padding: 31px 0px 31px 31px;
    height: 100%;
    &__logo {
      margin-bottom: 25px;
      width: 100px;
      img {
        width: 100px;
        filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg)
          brightness(102%) contrast(102%);
      }
    }

    &__links {
      display: flex;
      flex-direction: column;
      gap: 5px;
      height: 100%;
    }

    &__link {
      &__info {
        display: block;
        color: $Ohmyfood-white;
        display: flex;

        p {
          margin-left: 12px;
        }
      }
    }
  }
}
```

## Section 5. La palette du gout

### 9. header

- add [header](./menus/la_palette_du_gout/la_palette_du_gout.html)

```html
<!-- Logo -->
<header class="header__container">
  <div class="header">
    <ul class="header__links">
      <li class="header__link">
        <a href="#">
          <i class="fa-solid fa-arrow-left-long header__icon"></i>
        </a>
      </li>
      <li class="header__link">
        <a href="index.html" class="header__logo">
          <img
            src="../../images/logo/ohmyfood@2x.svg"
            alt=""
            class="header__logo__image"
          />
        </a>
      </li>
    </ul>
  </div>
</header>
<!-- end of Logo -->

<!-- Receipe section  -->
<div class="receipe__image">
  <img
    src="../../images/restaurants/restaurant1.jpg"
    alt=""
    class="receipe__image"
  />
</div>
<main>
  <!-- end of receipe section  -->
  <div class="main__receipe__container">
    <div class="main__receipe">
      <div class="main__receipe__title">
        <h1>La palette du goût</h1>
        <i class="fa-regular fa-heart main__receipe__icon"></i>
      </div>
    </div>
  </div>

  <!-- Hero  -->

  <!-- end of Hero -->
</main>
```

-style [header](./menus/la_palette_du_gout/styles/style_menu.scss)

```scss
header {
  background: #9356dc;
  //   @include flexbox-center();

  .header {
    width: 37.5rem;
    height: 6.4rem;
    box-shadow: $Ohmyfood-shadow-2;
    background: #99e2d0;

    &__icon {
      //   background: yellow;
      font-size: 20px;
    }

    &__links {
      display: flex;
      align-items: center;
      justify-content: space-around;
      background: #9356dc;
      height: 100%;
    }

    &__logo {
      display: block;
      //   background: #ff79da;
      img {
        width: 165px;
      }
    }
  }
}

.receipe__image {
  width: 37.5rem;
  background: #99e2d0;

  &__image {
    max-width: 100%;
    height: 500px;
  }
}
.main__receipe__container {
  position: relative;
  background: #000000;
}
.main__receipe {
  position: absolute;
  top: -35px;
  width: 37.5rem;
  padding-top: 4.2rem;
  background: #99e2d0;
  border-radius: 20px 20px 0 0;
  z-index: 1;
  &__title {
    display: flex;
    align-items: center;
    justify-content: space-around;
    h1 {
      font-family: "Shrikhand", cursive;
    }
  }

  &__icon {
    font-size: 20px;
  }
}
```

### 10. receipe entries

-fill [la_palette_du_gout](./menus/la_palette_du_gout/la_palette_du_gout.html)

-style [la_palette_du_gout](./menus/la_palette_du_gout/styles/style_menu.scss)

---

## Section 6. Le délice des sens

### 11. Le délice des sens

-fill [Le délice des sens](./menus/le_delice_des_sens/le_delice_des_sens.html)

-style [Le délice des sens](./menus/le_delice_des_sens/styles/style_menu.scss)

---

### 12.

-fill [Le délice des sens](./menus/le_delice_des_sens/le_delice_des_sens.html)

-style [Le délice des sens](./menus/le_delice_des_sens/styles/style_menu.scss)

---

## Section 7. La note enchantée & À la française

### 13. La note enchantée

-fill [La note enchantée](./menus/le_delice_des_sens/le_delice_des_sens.html)

-use style [La note enchantée](./menus/le_delice_des_sens/styles/style_menu.scss)

### 14. À la française

-fill [À la française](./menus/la_française/a_la_française.html)

-use style [À la française](./menus/la_française/styles/style_menu.scss)

---

## Section 8. Heart

### 15. Heart icon

- add [heart layout](./sass/layouts/heart.scss) and use it in [index.html](index.html) & [restaurants](./restaurants/)

```scss
.restaurant__menu__description__container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 30px;
  stroke-width: 30;
  stroke: black;
  fill: white;
  cursor: pointer;

  .heart {
    width: 30px;
    stroke-width: 30;
    stroke: black;
    fill: white;
    cursor: pointer;
  }

  .heart-full {
    position: absolute;
    fill: url(#text-fill);
    stroke: none;
  }
  .heart-empty {
    width: 30px;
    position: relative;
    &:hover {
      opacity: 0;
      transition: 0.5s;
    }
  }
}
```

## Section 9. Menu animation

### 16.Receipes animation

- add animation to receipes

```scss
@keyframes receipe-opacity {
  0% {
    opacity: 0;
  }

  25% {
    opacity: 0.25;
  }

  50% {
    opacity: 0.5;
  }

  75% {
    opacity: 0.75;
  }
  100% {
    opacity: 1;
  }
}

.show-receipe-with-opacity {
  animation: receipe-opacity 1s both;
}

#case-1 {
  animation-delay: 0.1s;
}

#case-2 {
  animation-delay: 0.2s;
}

#case-3 {
  animation-delay: 0.3s;
}

#case-4 {
  animation-delay: 0.4s;
}

#case-5 {
  animation-delay: 0.5s;
}

#case-6 {
  animation-delay: 0.6s;
}

#case-7 {
  animation-delay: 0.7s;
}

#case-8 {
  animation-delay: 0.8s;
}

#case-9 {
  animation-delay: 0.9s;
}
#case-10 {
  animation-delay: 1s;
}
```

## Section 10. tablet and desktop mediaqueries

### 17. Home Page tablet and desktop responsive attributes

- add [tablet mediaqueries](./sass/layouts/navigation.scss)

### 18. Restaurant tablet and desktop responsive attributes

- add [restaurants mediaqueries](./sass/layouts/navigation.scss)

### 19.

### 20.

---

## Section 12.

## Section 13.

## Section 14.

## Section 15.

## Section 16.

## Section 17.

## Section 18.

## Section 19.

## Section 20.
