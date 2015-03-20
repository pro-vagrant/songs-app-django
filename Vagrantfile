Vagrant.configure(2) do |config|
  config.vm.box = "django-v0.2.4"
  config.vm.box_url = "http://boxes.gajdaw.pl/django/django-v0.2.4.box"
  config.vm.box_download_checksum_type = "sha256"
  config.vm.box_download_checksum = "86637c21234ce0f4a563f665dba16776346299ebd59674a68328ff93f626404a"
  config.vm.network :forwarded_port, guest: 8000, host: 8000, host_ip: "127.0.0.1"

$script = <<SCRIPT

cd /vagrant/songs
python manage.py runserver 0.0.0.0:8000 >/dev/null 2>&1 &

SCRIPT

  config.vm.provision "shell", inline: $script, run: "always"

  config.vm.post_up_message = "The application is available at http://127.0.0.1:8000"
end
