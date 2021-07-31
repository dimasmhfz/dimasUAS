Vagrant.configure("2") do |config|
#Define LoadBalance
  config.vm.define "lb1" do |lb1|
    lb1.vm.box = "generic/ubuntu1804"
    lb1.vm.network "private_network", ip: "10.0.0.10"
    lb1.vm.provision "shell" do |s|
      s.path = "lb.sh"
    end
  end

#Define Web1
  config.vm.define "web1" do |web1|
    web1.vm.box = "generic/ubuntu1804"
    web1.vm.network "private_network", ip: "10.0.0.11"
    web1.vm.provision "shell" do |s|
      s.path = "web.sh"
      s.args = "1"
    end
  end

#Define Web2
  config.vm.define "web2" do |web2|
    web2.vm.box = "generic/ubuntu1804"
    web2.vm.network "private_network", ip: "10.0.0.12"
    web2.vm.provision "shell" do |s|
      s.path = "web.sh"
      s.args = "2"
    end
  end
end
