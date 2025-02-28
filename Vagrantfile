Vagrant.configure("2") do |config|

  machines = {
    "kquetat-S" => "192.168.56.110",
    "kquetat-SW" => "192.168.56.111"
  }

  machines.each do |machine_name, machine_ip|
    config.vm.define machine_name do |machine|
      machine.vm.box = "generix/alpine318"
      machine.vm.hostname = machine_name
      machine.vm.network "private_network", ip: machine_ip

      machine.vm.provider :virtualbox do |provider|
        provider.cpus = 1
        provider.memory = 512
      end
    end
  end

  # Configure SSH no pw
  config.ssh.insert_key = false
 
end
