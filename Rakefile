# encoding: utf-8
require 'rake/clean'
task :default => :server

desc 'Start the Jekyll server on http://localhost:4000/'
task :server do
  rm_rf '_site'
  puts 'jekyll serve --watch'
  exec 'jekyll serve --watch'
end

desc 'Rebuild site under _site with Jekyll'
task :jekyll do
  rm_rf '_site'
  sh 'jekyll'
end

CLEAN.include('_site', '_README.ru.rdoc')
