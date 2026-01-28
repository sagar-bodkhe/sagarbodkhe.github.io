# CSS Architecture Documentation

## Overview

The portfolio website has been refactored with a **modular CSS architecture** for better control, maintainability, and advanced visual effects.

## File Structure

```
assets/css/
├── base.css          # Variables, reset, typography, utilities
├── components.css    # Reusable components (buttons, cards, forms, etc.)
├── layout.css        # Navigation, grid system, flexbox utilities
├── sections.css      # Section-specific styles (hero, about, skills, etc.)
├── effects.css       # Advanced animations and special effects
└── responsive.css   # Media queries and responsive design
```

## Key Improvements

### 1. **Modular Organization**
- **base.css**: Design tokens, CSS variables, reset, typography
- **components.css**: Reusable UI components
- **layout.css**: Navigation and layout systems
- **sections.css**: Page sections styling
- **effects.css**: Animations and special effects
- **responsive.css**: Mobile-first responsive design

### 2. **Enhanced CSS Variables**
- Comprehensive design token system
- Color palette with variations (primary, secondary, accent)
- Spacing scale (0-32)
- Typography scale
- Transition and animation timing
- Z-index scale
- Shadow system

### 3. **Advanced Effects**

#### Animations
- Fade-in animations (with stagger delays)
- Float animations for orbs and icons
- Gradient text animations
- Scroll-triggered animations
- Hover effects with transforms

#### Visual Effects
- Glassmorphism (backdrop blur)
- Gradient borders
- Glow effects
- Shimmer effects
- Ripple effects
- 3D transforms
- Magnetic hover effects

### 4. **Component Enhancements**

#### Buttons
- Ripple effect on click
- Gradient backgrounds
- Smooth hover transforms
- Glow shadows

#### Cards
- Hover lift effect
- Gradient border on hover
- Smooth transitions
- Glassmorphism option

#### Social Links
- Animated background fill
- Icon rotation on hover
- Scale and lift effects

### 5. **Better Control**

#### CSS Custom Properties
All design values are now CSS variables, making it easy to:
- Change colors globally
- Adjust spacing consistently
- Modify animations
- Update typography

#### Utility Classes
- `.fade-in` - Scroll-triggered fade animation
- `.fade-in-delay-1` through `-5` - Staggered delays
- `.glow-on-hover` - Glow effect
- `.shimmer` - Shimmer animation
- `.glass` - Glassmorphism effect

## Usage Examples

### Changing Colors
```css
:root {
    --primary: #your-color;
    --secondary: #your-color;
}
```

### Adding Animation Classes
```html
<div class="skill-card fade-in fade-in-delay-2">
    <!-- content -->
</div>
```

### Using Glassmorphism
```html
<div class="card glass">
    <!-- content -->
</div>
```

## Performance

- CSS is split into logical modules for better caching
- Uses `will-change` for optimized animations
- Reduced motion support for accessibility
- Efficient selectors and minimal specificity conflicts

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- CSS Grid and Flexbox
- CSS Custom Properties
- Backdrop Filter (with fallbacks)

## Next Steps

1. Customize colors in `base.css` variables
2. Add more effects from `effects.css`
3. Adjust animations timing in variables
4. Extend components in `components.css`

## Migration Notes

The old `style.css` file is kept for reference but is no longer used. All styles have been migrated to the new modular structure.
