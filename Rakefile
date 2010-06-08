require 'rake'

desc "Let's hook this motherfucker into your system"
task :install do
  linkables = Dir.glob('*/**')

  linkables.each do |linkable|
    file = linkable.split('/').last.split('.').first
    unless File.directory?("#{ENV['HOME']}/.#{file}")
      `ln -s "$PWD/#{linkable}" "$HOME/.#{file}"`
    end
  end
end
