# Vagrant file in which the virtual machine ready to run docker containers on bootup

box = "ubuntu"
url = "http://files.vagrantup.com/precise64.box"
hostname = ""
ip = ""
ram = ""


Vagrant.configure("2") do |config|
  # All Vagrant configuration is done here.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = box

  # The url from where the 'conf.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = url
  
  # Hostname
  config.vm.host_name = hostname
  
  # Assign this VM to a host only network IP, allowing you to access it via the IP.
  config.vm.network :hostonly, ip

  # Customization
  config.vm.customize [
        'modifyvm', :id,
        '--name', hostname,
        '--memory', ram
      ]
  end

  config.vm.provider :virtualbox do |vb, override|
  end


  config.vm.provision "docker" do |docker|
    docker.pull_images "pathod" 
  
  	docker.run "pathod",
  	  # If not specified, then the container's default command will be used
  	  cmd: "bash -l",
  	  
  	  # Extra arguments for 'docker run' on the command line
  	  args: "-v '/vagrant:/var/www'"
  	
  end  
end


