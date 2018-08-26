require 'middleman-gh-pages'

desc 'Install dependencies'
task :install do
  system 'bundle install'
  system 'npm install -g browser-sync@2.23.5'
end

# Change basetheme.dev to your site path
desc 'Running Browsersync'
task :browsersync do
  system 'browser-sync start --proxy "wedding.local" --files "stylesheets/*.css, javascripts/*.js, source/**/*.slim" --no-inject-changes'
end

desc 'Watch sass'
task :sasswatch do
    system 'bundle exec sass -r sass-globbing --watch sass:css'
end

desc 'Serve'
task :serve do
  threads = []
    %w{sasswatch browsersync}.each do |task|
      threads << Thread.new(task) do |devtask|
        Rake::Task[devtask].invoke
      end
    end
  threads.each {|thread| thread.join}
  puts threads
end
