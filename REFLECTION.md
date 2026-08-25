## Part E — Reflection

### 1. CSS Rule

One important CSS rule is:

.services-container {
    display: flex;
}

If this rule was deleted, the three service cards would no longer be arranged in a horizontal Flexbox row. They would appear as normal block elements, changing the intended layout of the services section.

### 2. Flexbox vs Floats

Flexbox made it easier to arrange the three service cards in a row and control the spacing between them using the gap property. It also made it easier to stack the cards into a single column at the 520px breakpoint, which would be harder to achieve with floats.

### 3. Individual Reflection — Olinda Vashi

I owned Bug #0, which involved removing the alt attribute from the bicycle image. I learned that the missing alt attribute may not cause a visible change when the image loads, but it affects accessibility because there is no text alternative describing the image.