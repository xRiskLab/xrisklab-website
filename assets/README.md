# Assets Directory

This directory contains all static assets for the xRiskLab website.

## 📁 Directory Structure

```
assets/
├── css/                    # Stylesheets
│   └── style.css          # Main stylesheet
├── images/                # All image assets
│   ├── projects/          # Project screenshots/logos
│   │   ├── fastwoe.png
│   │   ├── woeboost.png
│   │   ├── xbooster.png
│   │   ├── fisher-scoring.png
│   │   ├── rf-explainer.png
│   │   ├── rfgboost.png
│   │   ├── catboost-incremental.png
│   │   └── pearsonify.jpeg
│   └── team/              # Team member photos
├── papers/                # Research papers and publications
│   ├── 2509.09855v1.pdf   # ArXiv paper on WOE standard errors
│   └── woe_standard_errors.pdf  # Technical report
└── docs/                  # Additional documentation
```

## �️ Image Guidelines

### Project Images
- **Dimensions**: Recommended 400x300px or similar 4:3 ratio
- **Format**: PNG or JPEG (PNG preferred for screenshots)
- **Size**: Keep under 500KB for web performance
- **Content**: Screenshots, logos, or visual representations of the project

### Team Photos
- **Dimensions**: 300x300px (square)
- **Format**: JPEG preferred
- **Size**: Keep under 200KB

## 📄 Papers & Documents

### Research Papers
- **Format**: PDF only
- **Naming**: Use descriptive names or ArXiv IDs
- **Size**: No strict limit, but consider loading times
- **Access**: All papers should be directly accessible via URL

### Documentation
- **Format**: PDF, Markdown, or other text formats
- **Organization**: Group by project or topic
- **Versioning**: Include version numbers in filenames when applicable

## � Linking Assets

### In Markdown Files
```markdown
![Project Screenshot](/assets/images/projects/fastwoe.png)
[Download Paper](/assets/papers/2509.09855v1.pdf)
```

### In Project Front Matter
```yaml
---
image: "/assets/images/projects/fastwoe.png"
paper: "/assets/papers/2509.09855v1.pdf"
---
```

### In HTML/Liquid Templates
```html
<img src="{{ '/assets/images/projects/fastwoe.png' | relative_url }}" alt="FastWoe">
<a href="{{ '/assets/papers/2509.09855v1.pdf' | relative_url }}">Download PDF</a>
```

## 🚀 Optimization Tips

1. **Compress Images**: Use tools like TinyPNG or ImageOptim before uploading
2. **Lazy Loading**: Large images should be optimized for web delivery
3. **CDN**: Consider using a CDN for frequently accessed files
4. **Caching**: Ensure proper cache headers for static assets

## 📝 Adding New Assets

1. **Place files in appropriate subdirectories**
2. **Use descriptive, lowercase filenames with hyphens**
3. **Update this README if adding new categories**
4. **Test links before committing**
5. **Optimize file sizes for web delivery**

## 🔧 File Management

- Keep file sizes reasonable for web delivery
- Use version control for tracking changes
- Remove unused assets periodically
- Maintain consistent naming conventions