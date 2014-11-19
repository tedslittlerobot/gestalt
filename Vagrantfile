VAGRANTFILE_API_VERSION = "2"

path = "#{File.dirname(__FILE__)}"

require 'yaml'
require path + '/gestalt/gestalt.rb'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # install ruby using rbenv manually (for now)
  config.vm.provision :shell, path: "https://raw.githubusercontent.com/wearearchitect/guides/master/homestead_ruby.sh", privileged: false

  Gestalt.configure(config, YAML::load(File.read(path + '/' + box + '.yaml')))
end
