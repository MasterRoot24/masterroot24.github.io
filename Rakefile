require 'html/proofer'

task :default => :spec

task :test => [:build] do
  HTML::Proofer.new('./_site',{
                                 :only_4xx => true,
                                 :check_favicon => true,
                                 :check_html => true
                             }).run
end

task :build do
  system 'bundle exec jekyll build'
end
