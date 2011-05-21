# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)
require 'rake'

# patch from http://stackoverflow.com/questions/5287121/undefined-method-task-using-rake-0-9-0-beta-4
# START PATCH
module ::Enki
  class Application
    include Rake::DSL
  end
end

module ::RakeFileUtils
  extend Rake::FileUtilsExt
end
# END PATCH

Enki::Application.load_tasks
