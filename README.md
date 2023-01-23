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

### 2. CSS and Fonts

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
$gradient: linear-gradient(
  180deg,
  rgba(255, 121, 218, 1) 0%,
  rgba(147, 86, 220, 1) 100%
);
```

- use Font Awesome library

```css
<script src="https://kit.fontawesome.com/85893a34ce.js" crossorigin="anonymous"></script>
```

- add [Ohmyfood! favicon](./images/logo/favico/ohmyfoodfavicon.png)

---
