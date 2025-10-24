# CSS Box Model Specifications - Header Component

## Header Container
```css
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 80px;
  background: rgba(0, 0, 0, 0.8);
  backdrop-filter: blur(6px);
  z-index: 1000;
  padding: 0 5%;
  display: flex;
  align-items: center;
}
```
- **Box Model**:
  - `width`: 100% (full viewport width)
  - `height`: 80px
  - `padding`: 0 5% (horizontal padding only)
  - `margin`: 0
  - `border`: none
  - `position`: fixed
  - `z-index`: 1000 (ensures header stays above other content)

## Logo Container
```css
.logo {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  height: 40px;
  display: flex;
  align-items: center;
}
```
- **Box Model**:
  - `width`: auto (based on image)
  - `height`: 40px
  - `position`: absolute
  - `left`: 50%
  - `transform`: translateX(-50%) (centers the logo precisely)
  - `margin`: 0
  - `padding`: 0

## Navigation Menu
```css
.nav {
  margin-left: auto;
  display: flex;
  align-items: center;
  height: 100%;
}

.nav__menu {
  display: flex;
  gap: 10px;
  list-style: none;
  margin: 0;
  padding: 0;
  height: 100%;
}

.nav__menu li {
  display: flex;
  align-items: center;
  position: relative;
  height: 100%;
}

.nav__menu a {
  color: white;
  text-decoration: none;
  text-transform: uppercase;
  font-size: 0.875rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  padding: 0 20px;
  height: 100%;
  display: flex;
  align-items: center;
  position: relative;
}
```
- **Navigation Container**:
  - `margin-left`: auto (pushes nav to the right)
  - `height`: 100% (matches header height)
  - `display`: flex
  - `align-items`: center

- **Menu Items**:
  - `gap`: 10px (space between items)
  - `padding`: 0 20px (horizontal padding for each link)
  - `height`: 100% (full header height)
  - `display`: flex
  - `align-items`: center

## Active/Hover States
```css
.nav__menu a::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 20px;
  right: 20px;
  height: 2px;
  background: #FFC000;
  transform: scaleX(0);
  transition: transform 0.2s ease;
}

.nav__menu a:hover::after,
.nav__menu a.current::after {
  transform: scaleX(1);
}
```
- **Underline Effect**:
  - `height`: 2px
  - `left/right`: 20px (matches link padding)
  - `bottom`: 0
  - `transform`: scales on hover/active

## Mobile Menu Button (Hamburger)
```css
.hamburger {
  display: none; /* Hidden on desktop */
  flex-direction: column;
  justify-content: space-between;
  width: 30px;
  height: 20px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  z-index: 1001;
}

.hamburger span {
  display: block;
  width: 100%;
  height: 2px;
  background: white;
  transition: all 0.3s ease;
}
```
- **Button**:
  - `width`: 30px
  - `height`: 20px
  - `padding`: 0
  - `margin`: 0
  - `border`: none
  - `z-index`: 1001 (above header)

## Responsive Breakpoints
```css
/* Tablet */
@media (max-width: 1023px) {
  .nav__menu {
    gap: 5px;
  }
  
  .nav__menu a {
    padding: 0 15px;
    font-size: 0.8rem;
  }
}

/* Mobile */
@media (max-width: 767px) {
  .nav__menu {
    position: fixed;
    top: 80px;
    right: -100%;
    width: 80%;
    max-width: 300px;
    height: calc(100vh - 80px);
    background: rgba(0, 0, 0, 0.95);
    flex-direction: column;
    align-items: flex-start;
    padding: 20px;
    transition: right 0.3s ease;
  }
  
  .nav__menu.open {
    right: 0;
  }
  
  .nav__menu li {
    width: 100%;
    height: auto;
  }
  
  .nav__menu a {
    padding: 15px 0;
    width: 100%;
  }
  
  .hamburger {
    display: flex;
  }
}
```
