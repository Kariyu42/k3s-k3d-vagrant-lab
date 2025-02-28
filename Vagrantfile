machine = {
  "kquetat-S" => "192.168.56.110",
  "kquetat-SW" => "192.168.56.111"
}

Vagrant.configure("2") do |config|

  # Configuration of the first machine
  config.vm.define "kquetat-S" do |server|
    server.vm.box = "generic/alpine318"
    server.vm.hostname = "kquetat-S"
    server.vm.network "private_network", ip: "192.168.56.110"
    server.vm.provider "virtualbox" do |vb|
      vb.cpus = "1"
      vb.memory = "512"
    end
  end

   # Configuration of the second machine
  config.vm.define "kquetat-SW" do |worker|
    worker.vm.box = "generic/alpine318"
    worker.vm.hostname = "kquetat-SW"
    worker.vm.network "private_network", ip: "192.168.56.111"
    worker.vm.provider "virtualbox" do |vb|
      vb.cpus = "1"
      vb.memory = "512"
    end
  end

  # Configure SSH no pw
  config.ssh.insert_key = false
 
end
