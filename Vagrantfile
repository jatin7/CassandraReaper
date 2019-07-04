Vagrant.configure("2") do |config|
  REAPER_NODES=2
  (1..REAPER_NODES).each do |reap|
    node_name = "reaper#{reap}"
    config.vm.define node_name do |reaper_node|
      reaper_node.vm.box = "centos/7"
      reaper_node.vm.network "private_network", ip: "192.168.43.#{200 + reap}"
      reaper_node.vm.hostname = node_name
      reaper_node.vm.provider :virtualbox do |vbox|
        vbox.linked_clone = true
        vbox.name = node_name
        vbox.memory = 3096
      end
      if reap == REAPER_NODES
          reaper_node.vm.provision :ansible do |ansible|
          ansible.limit = "all"
          ansible.playbook = "reaper.yml"
        end      end
    end
  end
end
