# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "sequel-cacheable"
  gem.homepage = "http://github.com/rosylilly/sequel-cacheable"
  gem.license = "MIT"
  gem.summary = %Q{This plug-in caching mechanism to implement the Model of the Sequel}
  gem.description = %Q{This plug-in caching mechanism to implement the Model of the Sequel}
  gem.email = "rosylilly@aduca.org"
  gem.authors = ["Sho Kusano <rosylilly>"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
  require 'simplecov'
  SimpleCov.start
  spec.pattern = 'spec/**/*_spec.rb'
end

task :default => :spec

require 'yard'
YARD::Rake::YardocTask.new