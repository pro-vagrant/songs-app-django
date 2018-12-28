Vagrant.configure(2) do |config|
  config.vm.box = "django-next-manual-build-v0.0.2"
  config.vm.box_url = "https://s3-eu-west-1.amazonaws.com/pro-vagrant/django-next-manual-build-v0.0.2.box"
  config.vm.box_download_checksum_type = "sha256"
  config.vm.box_download_checksum = "69c4fd1043766fff0bfe38497a164f9312c339b1710d7a47facaa43d89dca850"
  config.vm.network :forwarded_port, guest: 8000, host: 8000, host_ip: "127.0.0.1"

$script = <<SCRIPT

cd /vagrant/songs
python manage.py runserver 0.0.0.0:8000 >/dev/null 2>&1 &

SCRIPT

  config.vm.provision "shell", inline: $script, run: "always"

  config.vm.post_up_message = "The application is available at http://127.0.0.1:8000"
end
