VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.box = "gajdaw/django"
    config.vm.network :forwarded_port, guest: 8000, host: 8000, host_ip: "127.0.0.1"

end
