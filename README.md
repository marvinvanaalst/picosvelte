# Pico Svelte

Trying out how to design a minimal set of components using a PicoCSS-style approach.

```bash
npm install
npm run dev -- --open
```


## Definitions

We have the following CSS variables that are always available

```css
:root {
    /* Main colors */
    --l9: #ffffff;
    --light: #eff1f4;
    --dark: #202632;
    --l1: #000000;
    --primary: #0172ad;
    --secondary: #5d6b89;

}

/* Variables depending on light / dark mode */
[data-theme="light"] {
    --bg-default: var(--light);
    --bg-contrast: var(--dark);
    --bg-primary: var(--primary);
    --bg-secondary: var(--secondary);
}

[data-theme="dark"] {
    --bg-default: var(--l1);
    --bg-contrast: var(--light);
    --bg-primary: var(--primary);
    --bg-secondary: var(--secondary);
}

```
