# Custom Fonts - Matching Logo Typography

This guide shows you how to add custom fonts that exactly match your logo style.

## Current Implementation

The site currently uses **system fonts** with adjusted weights and spacing. This provides:
- ✅ Zero font loading time
- ✅ Native OS appearance
- ✅ Perfect performance
- ❌ Less exact logo match

## Adding Custom Fonts (Optional)

To exactly match your logo's bold, industrial typography:

### Option 1: Google Fonts (Recommended)

**For "SNAKE EYES" style (bold, condensed):**
- **Bebas Neue** - Closest match, free, popular
- **Oswald** (Extra Bold) - Similar condensed feel
- **Anton** - Very bold, similar impact

**For "SOFTWARE" style (geometric, clean):**
- **Rajdhani** (SemiBold/Bold) - Clean, geometric
- **Exo 2** - Tech-forward, modern
- **Orbitron** - Futuristic, geometric

### Implementation Steps

#### 1. Update `hugo.toml`

Add this section:

```toml
[params]
# Custom Google Fonts
customHead = '''
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
'''
```

#### 2. Update `assets/css/extended/custom.css`

Add to the top of the file:

```css
/* Custom Fonts - Logo Typography Match */
:root {
    --font-heading: 'Bebas Neue', 'Impact', sans-serif;
    --font-subheading: 'Rajdhani', 'Trebuchet MS', sans-serif;
    --font-body: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

/* Apply to headings */
h1, h2, h3, h4, h5, h6, .post-title {
    font-family: var(--font-heading);
    font-weight: 400; /* Bebas Neue only has 400 weight */
    letter-spacing: 0.02em; /* Slightly more open for web */
}

/* Apply to subheadings and labels */
.post-description, .section-subtitle, .post-meta,
.button, button, .menu a, .post-tags a {
    font-family: var(--font-subheading);
    font-weight: 600;
}

/* Body text remains system font */
body, p, li, article {
    font-family: var(--font-body);
}
```

#### 3. Test Performance

After adding fonts:

```bash
# Build the site
hugo

# Check file sizes
du -sh public/
```

Google Fonts are optimized and usually add < 50KB.

### Option 2: Self-Hosted Fonts

For complete control and privacy:

#### 1. Download Fonts

- Go to Google Fonts
- Select "Bebas Neue" and "Rajdhani"
- Click "Download family"
- Extract the files

#### 2. Add to Hugo

```bash
mkdir -p static/fonts
cp BebasNeue-Regular.ttf static/fonts/
cp Rajdhani-SemiBold.ttf static/fonts/
cp Rajdhani-Bold.ttf static/fonts/
```

#### 3. Update CSS

Add to `assets/css/extended/custom.css`:

```css
/* Self-hosted fonts */
@font-face {
    font-family: 'Bebas Neue';
    src: url('/fonts/BebasNeue-Regular.ttf') format('truetype');
    font-weight: 400;
    font-style: normal;
    font-display: swap;
}

@font-face {
    font-family: 'Rajdhani';
    src: url('/fonts/Rajdhani-SemiBold.ttf') format('truetype');
    font-weight: 600;
    font-style: normal;
    font-display: swap;
}

@font-face {
    font-family: 'Rajdhani';
    src: url('/fonts/Rajdhani-Bold.ttf') format('truetype');
    font-weight: 700;
    font-style: normal;
    font-display: swap;
}

/* Then use as in Option 1 */
:root {
    --font-heading: 'Bebas Neue', sans-serif;
    --font-subheading: 'Rajdhani', sans-serif;
}
```

### Option 3: Adobe Fonts (Commercial)

If you have Adobe Creative Cloud:

1. Go to fonts.adobe.com
2. Search for fonts similar to your logo
3. Activate them in your Adobe account
4. Add embed code to Hugo

### Option 4: Commercial Font Purchase

For exact logo match:

**Similar to "SNAKE EYES":**
- Agency FB (Microsoft)
- Impact (System font - already available!)
- Knockout (Hoefler&Co - commercial)
- Druk (Commercial Type - commercial)

**Similar to "SOFTWARE":**
- Eurostile (Linotype - commercial)
- Bank Gothic (System font - check availability)
- Microgramma (Linotype - commercial)

## Font Pairing Examples

### Combination 1: Bold & Geometric
```css
--font-heading: 'Bebas Neue', sans-serif;    /* Bold, compressed */
--font-subheading: 'Rajdhani', sans-serif;   /* Geometric, clean */
```
**Best for:** Matching your logo exactly

### Combination 2: Impact & Modern
```css
--font-heading: 'Impact', sans-serif;        /* System font, no load */
--font-subheading: 'Exo 2', sans-serif;      /* Futuristic */
```
**Best for:** Performance + modern feel

### Combination 3: All System Fonts
```css
--font-heading: 'Impact', sans-serif;
--font-subheading: 'Trebuchet MS', sans-serif;
```
**Best for:** Maximum performance (current setup)

## Recommended: Start Without Custom Fonts

Following "Keep It Simple":

1. **Launch with system fonts** (current setup)
2. **Test site performance and usability**
3. **Add custom fonts only if needed** for brand consistency
4. **Measure the impact** on load time and experience

The current CSS already achieves a similar feel to your logo through:
- Bold font weights (800)
- Condensed letter spacing
- Uppercase text
- Proper size hierarchy

## Performance Comparison

| Option | Load Time | Files | Pros | Cons |
|--------|-----------|-------|------|------|
| System Fonts | 0ms | 0 | Instant, native | Less brand match |
| Google Fonts | 50-100ms | 2-3 | Good match, reliable | External dependency |
| Self-Hosted | 20-50ms | 2-3 | Full control, privacy | Manual updates |
| Commercial | Varies | Varies | Exact match | Cost, licensing |

## Testing Your Font Choice

After implementing:

1. **Visual Test**
   - Compare headlines to logo
   - Check readability at different sizes
   - Test on mobile devices

2. **Performance Test**
   ```bash
   # Check page load time
   curl -w "@curl-format.txt" -o /dev/null -s "https://your-site.com"
   ```

3. **Accessibility Test**
   - Ensure contrast ratios remain compliant
   - Test with screen readers
   - Verify keyboard navigation

## My Recommendation

**Start with current setup (system fonts)**, then if you want closer logo matching:

1. Add **Bebas Neue** for headings (free, 20KB)
2. Add **Rajdhani** for subheadings (free, 30KB)
3. Total added weight: ~50KB
4. Visual impact: Much closer to logo
5. Performance impact: Minimal

This balances brand consistency with "Keep It Simple" philosophy.

## Quick Start - Add Custom Fonts Now

If you want to add fonts immediately:

```bash
# Edit Hugo config
# Add Google Fonts link to head
```

```toml
[params]
customHead = '''
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
'''
```

Then update your CSS (already created at `assets/css/extended/custom.css`):

```css
/* Add at the top */
h1, h2, h3, h4, h5, h6, .post-title {
    font-family: 'Bebas Neue', 'Impact', sans-serif !important;
}

.post-description, .section-subtitle, .post-meta, .button, .menu a {
    font-family: 'Rajdhani', 'Trebuchet MS', sans-serif !important;
}
```

Test locally:
```bash
hugo server -D
```

Visit http://localhost:1313 to see the difference!

---

**Note**: The current design already looks professional. Custom fonts are optional enhancement, not required.
