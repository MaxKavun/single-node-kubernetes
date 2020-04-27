Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/xenial64"
    master.vm.network "private_network", ip: "10.10.10.10"
    master.vm.provision "install_docker", type: "shell", path: "scripts/docker.sh"
    master.vm.provision "install_kubernetes", type: "shell", path: "scripts/master.sh"
  end
end