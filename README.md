# Rahul Kumar — Full-Time Web Developer

Hi, my name is Rahul Kumar and I am a full-time web developer. I have built 50+ websites for clients in the USA, UK, Australia, Singapore, and South Africa. I also enjoy writing blog posts in the WordPress and SEO niches and run a well-established YouTube channel. In February 2025, I launched my startup WPFixHub, which has been a successful venture.

## Skills & Focus
- WordPress Development (Web Development)
- SEO (Search Engine Optimization)
- Affiliate Marketing
- Blogging
- YouTube Recordings
- Online Courses Recordings

## Startup
- WPFixHub (founded February 2025)
- Company website: https://wp-fixhub.com/

## Photo & Profile
- Photo / Profile: https://wp-fixhub.com/rahul

## What I Do
- Design and develop responsive, performant websites
- Optimize sites for speed, accessibility, and search rankings
- Create content and tutorials for WordPress and SEO
- Produce educational recordings for YouTube and online courses

If you’re looking to build or improve a website, optimize SEO, or need help with WordPress, I’m happy to collaborate.

---

## Website Details — Online Admission Portal

### Overview
- A responsive, mobile‑ and desktop‑friendly admission portal UI.
- Clean header with college logo and support query text.
- Navigation bar with icons and clear links.
- Three content rows with colored boxes and images for key actions.
- Informational footer with policy notes and credits.

### Key Features
- Responsive layout (desktop, tablet, mobile breakpoints).
- Accessible nav links with inline SVG icons.
- Fluid images that adapt to container width.
- Simple, maintainable HTML + CSS without heavy frameworks.

### Navigation Items
- Home
- Online Application
- News
- Download Receipt
- Forgot Your Application ID
- Contact Us
- Login
- LMS

### Tech Stack
- HTML5
- CSS3 (Flexbox, media queries)
- Static hosting friendly (no backend requirement yet)

### Project Structure
```
.
├── index.html   # Main page
├── style.css    # Styles and responsive breakpoints
└── reade.md     # About + website details
```

### Assets
- Place images in the project root with these names:
  - `logo.png`, `migration.png`, `graduate-registration.png`, `pg-admission.png`,
    `clc.png`, `degree-exam-form.png`, `tc.png`.
- If not available, layout still renders with color blocks.

### How to Run Locally (Windows)
1) Easiest: open `index.html` directly in your browser.
2) PowerShell lightweight server (optional):
   - Open PowerShell in the project folder and run:
   ```powershell
   $folder = (Get-Location).Path
   $prefix = "http://localhost:5501/"
   Add-Type -AssemblyName System.Net
   $listener = New-Object System.Net.HttpListener
   $listener.Prefixes.Add($prefix)
   $listener.Start()
   Write-Host "Serving $folder at $prefix"
   while ($true) {
     $context = $listener.GetContext()
     $rel = $context.Request.Url.AbsolutePath.TrimStart('/')
     if ([string]::IsNullOrWhiteSpace($rel)) { $rel = 'index.html' }
     $path = Join-Path $folder $rel
     if (-not (Test-Path $path)) { $context.Response.StatusCode = 404; $context.Response.Close(); continue }
     $bytes = [System.IO.File]::ReadAllBytes($path)
     $context.Response.ContentType = 'text/html'
     $context.Response.OutputStream.Write($bytes,0,$bytes.Length)
     $context.Response.Close()
   }
   ```
3) Alternatives (if installed):
   - Python: `python -m http.server 5500`
   - Node: `npx http-server -p 5500`

### Deployment Tips
- Host on any static provider (Netlify, Vercel, GitHub Pages, or shared hosting).
- Ensure images are optimized and named exactly as referenced.
- Add real link targets for each nav item when backend/pages are ready.

### Credits
- Design and development: Rahul Kumar
- Company: WPFixHub — https://wp-fixhub.com/
