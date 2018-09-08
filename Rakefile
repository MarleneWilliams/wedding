require 'middleman-gh-pages'

# Setup / reset
# 'rake install'
desc 'Install dependencies'
task :install do
  system 'gem install bundler'
  system 'bundle install'
end

# Run Middleman server
# 'rake serve'
#
# Note: The most current version of Middleman breaks when trying to use the Livereload gem (see this GitHub issue: https://github.com/middleman/middleman/issues/2142). Some magic that might be explained here (https://github.com/egonSchiele/contracts.ruby) allows the addition of this exposed variable to help us get past the errors: `NO_CONTRACTS=true`.
#
desc 'Running Middleman server'
task :serve do
  system 'NO_CONTRACTS=true bundle exec middleman serve'
end

# Build site
# 'rake build'

# Publish to GitHub Pages
# 'rake publish'
