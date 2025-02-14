# culturessupports.github.io
javascripts blog jekyll


# Install Hugo (if not installed)
# macOS: brew install hugo
# Linux: sudo apt install hugo
# Windows: choco install hugo

# Create a new Hugo site
hugo new site my-hugo-blog
cd my-hugo-blog

# Add a theme (example: Ananke)
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke

# Configure Hugo
cat <<EOT >> config.toml
title = "My Hugo Blog"
baseURL = "https://example.com/"
theme = "ananke"
languageCode = "en-us"
paginate = 10
enableRobotsTXT = true

description = "A simple Hugo-powered blog."

[params]
  author = "Your Name"
  description = "Welcome to my Hugo blog!"
EOT

# Create a sample post
hugo new posts/first-post.md

echo "content/posts/first-post.md created. Edit the file to add content."

# Run the development server
hugo server -D
