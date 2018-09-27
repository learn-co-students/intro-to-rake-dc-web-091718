desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  desc "hello in English"
  task :hello do
    puts "hello from Rake!"
  end

  desc "hello in spanish"
  task :hola do
    puts "hola de Rake!"
  end
end


namespace :db do
  desc "migrate the db"
  task migrate: :environment do
    Student.create_table
  end

  desc "seed the database"
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc "requires the environment config file"
task :environment do
  require_relative './config/environment'
end

desc "drop into the pry console"
task console: :environment do
  Pry.start
end