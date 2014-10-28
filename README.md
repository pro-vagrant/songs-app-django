Songs for kids - django application
===================================

How to run the application?

Clone the repo:

    $ git clone https://github.com/pro-vagrant/songs-django-app.git
    $ cd songs-django-app

Boot VM:

    $ vagrant up
    $ vagrant ssh
    $ cd /vagrant

Start the server:

    $ cd songs
    $ python manage.py runserver 0.0.0.0:8000 &

Finally start your web browser and visit:

    http://127.0.0.1:8000

