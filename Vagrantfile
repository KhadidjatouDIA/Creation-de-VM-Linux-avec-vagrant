Vagrant.configure("2") do |config|
  config.vm.define "vg" do |vg|
    vg.vm.box = "bento/ubuntu-22.04"
    vg.vm.box_check_update = false
    vg.vm.network "forwarded_port", guest: 80, host: 8080
    vg.vm.network "private_network", ip: "192.168.33.10"
    vg.vm.synced_folder "./vg", "/vagrant_data"

    vg.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "1024"
      vb.name = "vg"
    end
  end
end
