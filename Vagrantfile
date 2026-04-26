Vagrant.configure("2") do |config|

  config.vm.box = "generic/oracle9"

  # Common provider settings
  config.vm.provider :libvirt do |lv|
    lv.driver = "qemu"   # 🔥 changed from kvm → qemu
  end

  # Node 1
  config.vm.define "dc-node1" do |node|
    node.vm.hostname = "dc-node1"

    node.vm.network "private_network",
                    ip: "192.168.56.11"

    node.vm.provider :libvirt do |lv|
      lv.memory = 2048
      lv.cpus   = 2
    end
  end

  # Node 2
  config.vm.define "dc-node2" do |node|
    node.vm.hostname = "dc-node2"

    node.vm.network "private_network",
                    ip: "192.168.56.12"

    node.vm.provider :libvirt do |lv|
      lv.memory = 2048
      lv.cpus   = 2
    end
  end

  # Node 3
  config.vm.define "dc-node3" do |node|
    node.vm.hostname = "dc-node3"

    node.vm.network "private_network",
                    ip: "192.168.56.13"

    node.vm.provider :libvirt do |lv|
      lv.memory = 2048
      lv.cpus   = 2
    end
  end

end