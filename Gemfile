require 'rbconfig'

source 'https://rubygems.org'

gemspec

gem 'bundler'

group :webservers do
  gem 'mongrel',  '~> 1.2.beta', :platform => [:mri, :rbx]
  gem 'reel', '~> 0.4.0.pre5'
  gem 'hatetepe', '~> 0.5.2'
end

group :guard do
  gem 'guard-rspec'
  case RbConfig::CONFIG['host_os']
  when /darwin/
    gem 'rb-fsevent'
    # gem 'growl_notify'
    gem 'growl'
  when /linux/
    gem 'rb-inotify'
    gem 'libnotify'
  end
end

group :docs do
  platform :mri_19, :mri_20 do
    gem 'redcarpet'
  end
end

platforms :jruby do
  gem 'jruby-openssl'
end

platform :rbx do
  gem 'rubysl'
  gem 'racc'
end
