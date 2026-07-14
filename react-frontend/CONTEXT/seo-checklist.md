# SEO & AI SEO Checklist for React Apps

> Essential SEO and Answer Engine Optimization (AEO) for React frontend applications.

---

## Traditional SEO for React

### Technical SEO
- [ ] Server-Side Rendering (SSR) or Static Site Generation (SSG) implemented
- [ ] Meta tags dynamically set per route
- [ ] Canonical URLs configured
- [ ] Sitemap generated and submitted
- [ ] Robots.txt configured
- [ ] Page load time < 3 seconds

### Content SEO
- [ ] Each page has unique H1
- [ ] Meta descriptions are compelling (150-160 chars)
- [ ] Title tags include primary keyword
- [ ] Images have alt text
- [ ] Internal linking structure is logical

---

## AI SEO / AEO for React Apps

### Why AI SEO Matters
40%+ of users now ask AI systems (ChatGPT, Perplexity) for recommendations. Your app should be discoverable by these systems.

### AI SEO Quick Wins

**1. Clear Entity Definition**
```jsx
// In your homepage/main component
const description = "[App Name] is a [category] that helps [audience] [outcome]";

// Meta tag
<meta name="description" content={description} />
```

**Check:** First paragraph on homepage clearly states what the app is.

**2. Structured Data**
Add to your HTML head:
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebApplication",
  "name": "App Name",
  "applicationCategory": "[Category]Application",
  "description": "[Clear description]",
  "offers": {
    "@type": "Offer",
    "price": "[price]",
    "priceCurrency": "USD"
  }
}
</script>
```

**3. FAQ Section with Schema**
Create FAQ component with structured data:
```jsx
const faqData = {
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is [App Name]?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Answer]"
      }
    }
  ]
};
```

**4. Entity-Rich Content**
- Use precise category names ("project management app" not "tool")
- Mention related concepts naturally
- Answer common questions in content

---

## Implementation Checklist

### Pre-Launch
- [ ] Homepage H1 clearly defines app category
- [ ] Meta tags dynamically generated per route
- [ ] Schema markup added to index.html
- [ ] FAQ page/component created with structured data
- [ ] Page speed optimized (Core Web Vitals)

### Post-Launch
- [ ] Submit sitemap to Google Search Console
- [ ] Test with ChatGPT: "What is [App Name]?"
- [ ] Test with Perplexity: search app category
- [ ] Document baseline AI visibility

### Ongoing
- [ ] Monthly AI visibility check (ask AI about your app)
- [ ] Content freshness review (quarterly)
- [ ] Schema markup validation

---

## React-Specific SEO Tools

### Recommended Libraries
- `react-helmet` or `react-helmet-async` — Dynamic meta tags
- `next/head` (if using Next.js) — Built-in SEO
- `react-schemaorg` — Structured data components

### Code Example: SEO Component
```jsx
import { Helmet } from 'react-helmet-async';

function SEO({ title, description, schema }) {
  return (
    <Helmet>
      <title>{title}</title>
      <meta name="description" content={description} />
      <script type="application/ld+json">
        {JSON.stringify(schema)}
      </script>
    </Helmet>
  );
}
```

---

## AI Visibility Testing

### Monthly Questions to Ask AI
1. "What is [App Name]?"
2. "Best [category] apps"
3. "[App Name] vs [competitor]"

### Track Results
| Date | Platform | Query | Mentioned? | Notes |
|------|----------|-------|------------|-------|
| 2024-01 | ChatGPT | What is X? | Yes/No | |

---

## Related Resources

- `_PATTERNS/COURSE-INSIGHTS/jamie-garside-ai-seo-visibility-playbook.md`
- `client-website/SITE/ai-visibility.md` (detailed guide)
- `saas-micro/LANDING/ai-seo-optimization.md` (SaaS-specific)
