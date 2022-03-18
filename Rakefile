
desc 'outputs hello to the terminal'

task :environment do
  require_relative './config/environment'
end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end

namespace :greeting do 
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end

  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end
end