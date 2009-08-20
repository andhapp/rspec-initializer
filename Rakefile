namespace :initialize do
      
  desc "Initializes RSpec in this directory"
  task :rspec => :create_spec_options_file do
    puts "rspec initialized"
  end
  
  desc "creates the spec directory where this rake command is run"
  task :create_spec_directory do
    Dir.mkdir('./spec') if !test ?d, './spec'
  end
  
  desc "creates the spec_helper file"
  task :create_spec_helper_file => :create_spec_directory do
      File.open('./spec/spec_helper.rb', 'w') {|file| file.write "require 'spec/autorun'\nSpec::Runner.configure do |config|\nend"}
  end
  
  desc "creates the spec options file"
  task :create_spec_options_file => :create_spec_helper_file do
    File.open('./spec/spec.opts', 'w') { |file| file.write "--format specdoc \n--colour"}
  end
  
end
