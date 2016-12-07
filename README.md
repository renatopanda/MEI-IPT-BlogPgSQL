# Rails5 Blog using Postgres + Vagrant
## MEI-IoT Software Engineering

A simple academic demo about how to use Vagrant in rails development. The project is simply an adaptation of the Rails5 Blog tutorial (from the getting started guide), this time using Postgres and Bootstrap.

To start, with vagrant, virtualbox and git installed:
```
git clone https://github.com/renatopanda/MEI-IPT-BlogPgSQL.git
cd MEI-IPT-BlogPgSQL
vagrant up <see note below>
vagrant ssh
cd /vagrant
bundle install
rails db:setup
rails server –bind 0.0.0.0
```



Note: the last version of the public box used in this exercise (jadesystems/rails5) gives an error during provisioning. You will probably get a "Could not get lock /var/lib/dpkg/lock" during the "vagrant up". To fix it, simply delete the lock file and restart the setup:
```
vagrant ssh
sudo rm /var/lib/apt/lists/lock
logout
vagrant reload
```
