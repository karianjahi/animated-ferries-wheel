# Animated Ferris Wheel

A visually engaging **Ferris wheel animation** built entirely with HTML and CSS. This project demonstrates how to create smooth rotation animations for both a wheel structure and its cabins, using CSS keyframes and transforms.

---

## Table of Contents

- [Demo](#demo)  
- [Features](#features)  
- [Technologies Used](#technologies-used)  
- [Project Structure](#project-structure)  
- [How It Works](#how-it-works)  
- [Customization](#customization)  
- [License](#license)  

---

## Demo

![Ferris Wheel Animation](images/animation-wheel.gif)  


---

## Features

- **Full rotation animation** of the Ferris wheel using CSS keyframes.  
- **Cabins with independent animations**: rotate and change colors over time.  
- **Responsive design**: scales up to 55% of viewport width and height, with a max size of 500px.  
- **Pure CSS solution**: no JavaScript required.  

---

## Technologies Used

- HTML5  
- CSS3 (Animations, Keyframes, Transformations)  

---

## Project Structure
```
    animation-ferries-wheel/
                    ├── images/
                    │   └── animation-wheel.gif
                    ├── .gitignore
                    ├── index.html
                    ├── styles.css
                    └── README.md
```

---

## How It Works

### 1. The Wheel

- The wheel is represented by a circular `<div>` with the class `.wheel`. It has:

- **Border and border-radius** to form a circle.
- **Rotation animation** using the `@keyframes wheel` rule:

```css
    @keyframes wheel {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(900deg); }
    }
```
- The wheel rotates continuously with linear timing over 60 seconds.

### 2. Spokes of the Wheel
- Implemented with `<span class="line"></span>` elements.

- Each line is positioned absolutely with transform-origin at the center of the wheel.

- Lines are rotated in 60° increments to form the spokes:

```css
    .line:nth-of-type(2) { transform: rotate(60deg); }
    .line:nth-of-type(3) { transform: rotate(120deg); }
```


### 3. The Cabins
- Each cabin is a <div class="cabin"></div> positioned around the wheel.

- Cabins rotate individually using the `@keyframes cabins` animation:

```css
    @keyframes cabins {
        0% { transform: rotate(0deg); }
        25% { background-color: yellow; }
        50% { background-color: purple; }
        75% { background-color: yellow; }
        100% { transform: rotate(-360deg); }
    }
```

- Cabins change color over time while counter-rotating to stay upright relative to the viewer.

- Absolute positioning ensures cabins appear at proper locations around the wheel.

## Customization
- You can easily customize this animation:

- **Wheel size:** Adjust `.wheel` `height` and `width`.

- **Rotation speed:** Change animation-duration for `.wheel` or `.cabin`.

- **Cabin colors:** Modify colors inside `@keyframes cabins`.

- **Number of cabins/spokes:** Add or remove <div class="cabin"> or <span class="line"> elements and adjust rotations accordingly.

## License
This project is licensed under the MIT License. Feel free to use, modify, and share!

## Conclusion
This project demonstrates how CSS transformations and keyframe animations can create complex motion effects like a Ferris wheel with rotating, color-changing cabins — all without JavaScript. It’s a great starting point for learning animation techniques and creative CSS design.