# Jonathan Stronach's Blog

A personal blog built with Jekyll and the Minimal Mistakes theme, optimized for GitHub Pages hosting.

## Features

- Clean, responsive design using Minimal Mistakes theme
- SEO optimized with sitemap and meta tags
- Blog post management with categories and tags
- Prose.io integration for easy content editing
- GitHub Pages ready

## Local Development

### Prerequisites

- Ruby (version 2.5.0 or higher)
- RubyGems
- GCC and Make

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/jon-stronach-blog.git
cd jon-stronach-blog
```

2. Install Jekyll and dependencies:
```bash
gem install bundler
bundle install
```

3. Run the site locally:
```bash
bundle exec jekyll serve
```

4. Open your browser and navigate to `http://localhost:4000`

### Development Commands

- **Build the site**: `bundle exec jekyll build`
- **Serve with live reload**: `bundle exec jekyll serve --livereload`
- **Build for production**: `JEKYLL_ENV=production bundle exec jekyll build`

## Content Management

### Creating New Posts

1. **Via Prose.io** (Recommended):
   - Navigate to [prose.io](https://prose.io)
   - Authorize with your GitHub account
   - Navigate to the `_posts` folder
   - Click "New File" and start writing

2. **Manually**:
   - Create a new file in `_posts/` directory
   - Name it following the pattern: `YYYY-MM-DD-title-of-post.md`
   - Add the required front matter:
   ```yaml
   ---
   title: "Your Post Title"
   date: YYYY-MM-DD
   categories:
     - Category1
     - Category2
   tags:
     - tag1
     - tag2
   excerpt: "Brief description of your post"
   ---
   ```
   - Write your content in Markdown

### Creating New Pages

1. Create a new file in `_pages/` directory
2. Add front matter with at minimum:
   ```yaml
   ---
   title: "Page Title"
   permalink: /page-url/
   layout: single
   ---
   ```

## Deployment to GitHub Pages

1. Push your changes to GitHub:
```bash
git add .
git commit -m "Your commit message"
git push origin main
```

2. Enable GitHub Pages:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select source: "Deploy from a branch"
   - Choose branch: `main` (or `gh-pages` if you prefer)
   - Select folder: `/ (root)`

3. Your site will be available at: `https://yourusername.github.io/jon-stronach-blog/`

## Customization

### Site Configuration

Edit `_config.yml` to customize:
- Site title and description
- Author information
- Social media links
- Theme settings

### Theme Customization

- Change theme skin in `_config.yml` (options: "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise")
- Custom CSS: Create `assets/css/main.scss` and add your styles
- Custom JavaScript: Add files to `assets/js/` directory

## SEO Features

This site includes:
- XML sitemap (auto-generated)
- SEO meta tags
- Open Graph tags for social sharing
- Structured data markup
- Clean URLs
- Mobile-responsive design

## Prose.io Configuration

This blog is configured to work with Prose.io for easy content editing:
- Default metadata for posts
- Predefined categories and tags
- Media upload to `assets/images/`

## Directory Structure

```
jon-stronach-blog/
├── _config.yml          # Site configuration
├── _data/              # Data files
│   └── navigation.yml  # Navigation menu
├── _pages/             # Static pages
├── _posts/             # Blog posts
├── assets/             # Images, CSS, JS
├── _prose.yml          # Prose.io configuration
├── Gemfile             # Ruby dependencies
└── index.html          # Homepage
```

## Troubleshooting

### Bundle Install Fails
- Make sure you have Ruby development headers: `sudo apt-get install ruby-dev` (Ubuntu/Debian)
- On macOS, install Xcode Command Line Tools: `xcode-select --install`

### Jekyll Serve Fails
- Check Ruby version: `ruby -v` (should be 2.5.0+)
- Clear Jekyll cache: `bundle exec jekyll clean`
- Reinstall dependencies: `bundle install --force`

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For questions or suggestions, please open an issue on GitHub or contact through the social links on the website.