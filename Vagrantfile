# -*- mode: ruby -* 
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.box = "generic/ubuntu1804"
    config.ssh.insert_key = false
    config.vm.synced_folder ".", "/vagrant", disabled: true
    config.vm.provider :virtualbox do |v|
        v.memory = 1024
        v.linked_clone = true
        v.gui = true
    end

    # App Server 1
    config.vm.define "srv1" do |app|
        app.vm.box = "generic/ubuntu1804"
        app.vm.hostname = "app.test"
        app.vm.network :private_network, ip: "192.168.56.4"
    end

    # # App Server 2
    # config.vm.define "srv2" do |db|
    #     db.vm.box = "generic/ubuntu1804"
    #     db.vm.hostname = "db.test"
    #     db.vm.network :private_network, ip: "192.168.56.5"
    # end

    # # App Server 3
    # config.vm.define "srv3" do |monitoring|
    #     monitoring.vm.box = "generic/ubuntu1804"
    #     monitoring.vm.hostname = "monitoring.test"
    #     monitoring.vm.network :private_network, ip: "192.168.56.6"
    # end

    #  # App Server 4
    #  config.vm.define "srv4" do |rhel|
    #      rhel.vm.box = "generic/rhel8"
    #      rhel.vm.hostname = "rhel.test"
    #      rhel.vm.network :private_network, ip: "192.168.56.7"
    # end
end

