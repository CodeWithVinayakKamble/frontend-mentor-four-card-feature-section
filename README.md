# Frontend Mentor - Four Card Feature Section

## Built With

- Semantic HTML5
- Vanilla CSS
- CSS Custom Properties (Variables)
- Strict BEM Naming Convention (e.g., `feature-box__multi-card-wrapper`)
- `clamp()` for fluid font sizes for all screen sizes.
- Flexbox (Used for mobile layouts and internal card alignment)
- CSS Grid (Used for the desktop cross-shape layout)
- Mobile-First Workflow

## What I Learned

During this project, I significantly improved my layout strategies and problem-solving skills. Here are my biggest takeaways:

**1. The Grid + Flexbox Combo for Complex Layouts:**
Instead of struggling with a complicated 3x3 CSS Grid to create the desktop "cross" shape, I learned how to combine tools. By grouping the middle two cards inside a Flexbox wrapper (`.feature-box__multi-card-wrapper`), I was able to use a simple 3-column CSS Grid (`grid-template-columns: repeat(3, 1fr)`) and `place-items: center` to perfectly align the outer cards.

**2. Fixing the "Sticky Hover" Bug on Mobile:**
I discovered a common quirk where touch devices "fake" a hover state when tapped, leaving elements stuck in their hover appearance. I learned to fix this by using a special media query to only apply hover effects to devices with real mice:
```css
@media (hover: hover) {
  .feature-card:hover {
    transform: scale(1.1);
  }
}
```
I then used the `:active` pseudo-class separately to handle touch interactions on mobile.

**3. Mastering Box Shadows:**
Instead of relying on generators, I learned the manual syntax of `box-shadow` (`x y blur spread color`) to create soft, modern shadows using transparent `rgba` colors mapped to CSS variables.

## Author

- Challenge by Frontend Mentor
- Coded by **Vinayak Kamble**
