Vagrant.configure(2) do |config|

    N = 3
    (1..N).each do |i|
      config.vm.define "pxc#{i}" do |node|
        node.vm.box = "ubuntu/jammy64"
        node.vm.synced_folder ".", "/vagrant", disabled: true
        node.vm.hostname = "pxc#{i}"
        node.vm.network "private_network", ip:"10.0.26.20#{i}"
        node.vm.provider "virtualbox" do |vb|
          vb.memory = "1024"
          vb.name = "pxc#{i}"
          vb.cpus = 2
        end
      end
    end
 
end