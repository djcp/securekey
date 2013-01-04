require 'rubygems'
require 'rake'
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new do |t|
  t.rspec_opts = ["-c", "-f progress", "-r ./spec/spec_helper.rb"]
  t.pattern = 'spec/**/*_spec.rb'
end

task :default => :spec

require './app/secure_key'
desc 'rotate all'
task :rotate do
  puts 'starting rotations'
  User.rotatable.each do |u|
    begin
      puts "rotating #{u.id} (#{u.plan}): #{u.heroku_id}"
      u.rotate_keys!
      puts "  success!"
    rescue => e
      puts "  failed #{e.inspect}"
      next
    end
  end
  puts 'finished'
end


