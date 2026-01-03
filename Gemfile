source "https://rubygems.org"

# Use the latest Jekyll (Fixes Ruby 3.4 compatibility issues)
gem "jekyll", "~> 4.4.1"

# Default theme
gem "minima", "~> 2.5"

# PLUGINS
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-seo-tag"  
  gem "jekyll-sitemap"  
end

# RUBY 3.4 COMPATIBILITY FIXES (CRITICAL)
gem "csv", "~> 3.3"
gem "base64", "~> 0.3.0"
gem "bigdecimal", "~> 4.0"
gem "mutex_m", "~> 0.3.0"
gem "drb", "~> 2.2"
gem "erb", "~> 4.0"     # <--- This is the one causing your current crash
gem "logger", "~> 1.6"  # <--- This fixes the warning messages

# Windows/Timezone fixes
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]
