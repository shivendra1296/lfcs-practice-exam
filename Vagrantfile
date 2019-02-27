Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.define "home" do |home|
    home.vm.hostname = "home"
    home.vm.network "private_network", ip: "1.2.3.4"
    home.vm.provision "Home", type: "ansible" do |a|
      a.playbook = "roles/home.yml"
    #  a.tags = "execute"
    end
  end
  config.vm.define "server1" do |s1|
    s1.vm.hostname = "server1"
    s1.vm.network "private_network", ip: "1.2.3.5"
    s1.vm.provision "Server1", type: "ansible" do |a|
      a.playbook = "roles/server1.yml"
      # a.tags = "execute"
    end
  end
  config.vm.define "server2" do |s2|
    s2.vm.hostname = "server2"
    s2.vm.network "private_network", ip: "1.2.3.6"
    s2.vm.provision "Server2", type: "ansible" do |a|
      a.playbook = "roles/server2.yml"
    #  a.tags = "execute"
    end
  end
end
