Vagrant.configure("2") do |config|
  # Specify the provider
  config.vm.provider "vmware_desktop" do |v|
    v.vmx["cpuid.coresPerSocket"] = "2"
    v.memory = 2048
  end

  # Main node configuration
  config.vm.define "main" do |main|
    main.vm.box = "bento/ubuntu-20.04-arm64"
    main.vm.hostname = "main"
    main.vm.network "public_network", ip: "192.168.1.10"  # Adjust IP range as needed for your network
  end

  # Node1 configuration
  config.vm.define "node1" do |node1|
    node1.vm.box = "bento/ubuntu-20.04-arm64"
    node1.vm.hostname = "node1"
    node1.vm.network "public_network", ip: "192.168.1.11"
  end

  # Node2 configuration
  config.vm.define "node2" do |node2|
    node2.vm.box = "bento/ubuntu-20.04-arm64"
    node2.vm.hostname = "node2"
    node2.vm.network "public_network", ip: "192.168.1.12"
  end
end
