namespace :greeting do
  desc 'outputs hello to the terminal'
    task :hello do
      puts "hello from Rake!"
    end

  desc 'outputs hola to the terminal'
    task :hola do
      puts "hola from Rake!"
    end
end

task :environment do
  require_relative './config/environment'
end

desc 'migrate changes to the database'
  namespace :db do
    task :migrate => :environment do
      Student.create_table
    end
  end

desc 'seed some dummy data into the database'
  namespace :db do
    task :seed do
      require_relative "./db/seeds.rb"
    end
  end

desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end
