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

- [create a pull request]()

---

## Section 2. Header

### 3.

### 4.

### 5.

### 6.

### 7.

### 8.

### 9.

### 10.

### 11.

### 12.

### 13.

### 14.

### 15.

### 16.

### 17.

### 18.

### 19.

### 20.

---

## Section 3.

## Section 3.

## Section 4.

## Section 5.

## Section 6.

## Section 7.

## Section 8.

## Section 9.

## Section 10.

## Section 11.

## Section 12.

## Section 13.

## Section 14.

## Section 15.

## Section 16.

## Section 17.

## Section 18.

## Section 19.

## Section 20.
