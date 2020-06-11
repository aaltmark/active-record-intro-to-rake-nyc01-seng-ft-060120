namespace :greeting do 
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'outputs hola to the terminal' #greeting and hola now grouped 
task :hola do 
  puts "hola de Rake!"
end 
end 

task :environment do 
  require_relative './config/environment' #gives accesss to file (needed below )
end 

namespace :db do #db namespace will have a number of database-related tasks 
  desc 'migrate changes to your database'
  task :migrate => :environment do
      Student.create_table 
  end 
  desc 'seed the database with some dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
  end 
end  

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

