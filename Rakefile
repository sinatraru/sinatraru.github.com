require 'rake/clean'

task :default => :server

desc 'Start the Jekyll server on http://localhost:4000/'
task :server do
  rm_rf '_site'
  puts 'jekyll --pygments --auto --server'
  exec 'jekyll --pygments --auto --server'
end

desc 'Rebuild site under _site with Jekyll'
task :jekyll do
  rm_rf '_site'
  sh 'jekyll --pygments'
end

CLEAN.include('_site')
