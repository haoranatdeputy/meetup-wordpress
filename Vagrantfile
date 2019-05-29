# This is Scotchbox.

Vagrant.configure("2") do |config|
  config.vm.box = "scotch/box"
  config.vm.network "private_network", ip: "11.11.11.11"
  config.vm.hostname = "scotchbox"
  config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]
  config.vm.synced_folder "_vagrant/", "/etc/apache2/sites-enabled/", 
    type: "rsync", 
    rsync__args: ["-r", "--include=meetup.conf", "--exclude=*"]
end
