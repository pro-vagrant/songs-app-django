VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.box = "http://boxes.gajdaw.pl/django/django-v0.2.4.box"
    config.vm.network :forwarded_port, guest: 8000, host: 8000, host_ip: "127.0.0.1"

$script = <<SCRIPT

cd /vagrant/songs
python manage.py runserver 0.0.0.0:8000 >/dev/null 2>&1 &

SCRIPT

  config.vm.provision "shell", inline: $script, run: "always"

end
