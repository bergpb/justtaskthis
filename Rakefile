# frozen_string_literal: true

require 'rake/testtask'
require 'sinatra/activerecord/rake'
require File.dirname(__FILE__) + '/app'

desc 'Run server with shotgun'
task :serve do
  sh 'shotgun config.ru'
end

desc 'Run Slim linter'
task :slim_linter do
  sh 'slim-lint views'
end

task default: 'test'
Rake::TestTask.new do |t|
  t.pattern = 'tests/*_test.rb'
  t.verbose = false
  t.warning = false
end
