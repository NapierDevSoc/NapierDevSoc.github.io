require "rubygems"
require "rake"
require 'rubygems'
require 'optparse'
require 'yaml'

desc "Automatically generate site at :4000 for local dev"
task :dev do
  system "jekyll serve --watch"
end # task :dev

desc "Remove _site from directory before commiting"
task :clean do
  system "rm -rf _site"
end # taks :clean

desc "Create a new post"
task :post do
  OptionParser.new.parse!
  ARGV.shift
  title = ARGV.join(' ')

  path = "_posts/#{Date.today}-#{title.downcase.gsub(/[^[:alnum:]]+/, '-')}.md"
  
  if File.exist?(path)
        puts "[WARN] File exists - skipping create"
  else
    File.open(path, "w") do |file|
      file.puts YAML.dump({'layout' => 'post', 'published' => false, 'title' => title})
      file.puts "---"
    end
  end

  exit 1
end
