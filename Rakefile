require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name        = "teambox-client"
    gem.summary     = "A ruby gem wrapper for Teambox API"
    gem.description = "Provides methods to read and write to Teambox for ruby apps"
    gem.email       = "pablo@teambox.com"
    gem.homepage    = "http://github.com/teambox/teambox-ruby-client"
    gem.authors     = ["Pablo Villalba", "James Urquhart"]

    # 2013-07-09 - Attempting to bump httparty from ~> 0.7.4
    gem.add_dependency("httparty", "~> 0.10.0")
    # 2013-07-09 - Attempting to bump oauth2 from ~> 0.1.1
    gem.add_dependency("oauth2", "~> 0.8.0")
    # 2013-07-09 - Attempting to bump json from ~> 1.5.1
    gem.add_dependency("json", "~> 1.8.0")
  end
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new do |t|
  t.pattern = "spec/*spec.rb"
end

task :default => :spec

# ERROR: 'rake/rdoctask' is obsolete and no longer supported. Use 'rdoc/task' (available in RDoc 2.4.2+) instead.
require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  if File.exist?('VERSION')
    version = File.read('VERSION')
  else
    version = ""
  end

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "teambox-client #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/**/*.rb')
end
