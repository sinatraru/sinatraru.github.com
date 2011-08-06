require 'rake/clean'
require 'rdoc/markup/to_html'
require 'uri'

task :default => :server

# generates Table of Contents
def with_toc(src)
  toc = "<div class=\"toc\">\n"
  last_level = 1
  src = src.gsub(/<h(\d)>(.*)<\/h\d>/) do |line|
    level, heading = $1.to_i, $2.strip
    aname = URI.escape(heading)
    toc << "\t"*last_level << "<ol class='level-#{level-1}'>\n" if level > last_level
    toc << "\t"*level << "</ol>"*(last_level - level) << "\n" if level < last_level
    toc << "\t"*level << "<li><a href='##{aname}'>#{heading}</a></li>\n"
    last_level = level
    "<a name=\"#{aname}\"></a>\n" << line
  end
  toc << "\t" << "</ol>"*(last_level-1) << "\n</div>\n"
  toc + src
end

namespace :readme do
  desc "Pull in the latest README.ru.rdoc"
  task :pull do
    sh 'curl -s https://raw.github.com/vast/sinatra/master/README.ru.rdoc > _README.ru.rdoc'
  end

  desc "Build _includes/README.ru.html"
  task :build => :pull do
    puts "_README.ru.rdoc => _include/README.ru.html"
    html = RDoc::Markup::ToHtml.new.convert(File.read("_README.ru.rdoc")).
           sub("<h1>Sinatra</h1>", "").
           sub(/(английской версии)/, "<a href=\"http://sinatrarb.com/intro\">\\1</a>").
           gsub("<pre>", "<pre><code>").
           gsub("</pre>", "</code></pre>")

    File.open('_includes/README.ru.html', 'wb') {|f| f.write(with_toc(html))}
  end
end

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

CLEAN.include('_site', '_README.ru.rdoc')
