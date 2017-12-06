# Load DSL and Setup Up Stages
require 'capistrano/setup'
require 'capistrano/deploy'

require "capistrano/scm/git"
    install_plugin Capistrano::SCM::Git
    
require 'capistrano/rails'
require 'capistrano/bundler'
require 'capistrano/rvm'
require 'capistrano/puma'

    install_plugin Capistrano::Puma, load_hooks: false  # Default puma tasks without hooks
    install_plugin Capistrano::Puma::Monit, load_hooks: false  # Monit tasks without hooks

# Loads custom tasks from `lib/capistrano/tasks' if you have any defined.
Dir.glob('lib/capistrano/tasks/*.rake').each { |r| import r }