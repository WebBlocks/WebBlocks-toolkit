require 'rubygems'
require 'bundler'

begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end

task 'initialize' do
  system "node_modules/bower/bin/bower install"
end

if File.exists? 'bower_components/WebBlocks-rake/lib/Rake.rb'
  require 'extensions/kernel' if defined?(require_relative).nil?
  require_relative 'bower_components/WebBlocks-rake/lib/Rake'
end
