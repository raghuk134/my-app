Vagrant.configure("2") do |config|

   config.vm.define "node1" do |node1|
   node1.vm.box = "bento/centos-6.7"
   node1.vm.hostname = "node1.mylab.local"
   node1.vm.network :private_network, ip: "192.168.56.11"
   config.vm.provision "shell", inline: <<-SHELL
    apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'
apt-get update
apt-get install -y docker.io
systemctl enable docker
systemctl start docker
usermod -aG docker ubuntu
    	
  SHELL
   end

   config.vm.define "node2" do |node2|
   node2.vm.box = "centos/7"
   node2.vm.hostname = "node2.mylab.local"
   node2.vm.network :private_network, ip: "192.168.56.12"
   config.vm.provision "shell", inline: <<-SHELL
    sudo yum install epel-release
    sudo yum update
     
  SHELL
   end
   
   config.vm.define "node3" do |node3|
   node3.vm.box = "ubuntu/trusty64"
   node3.vm.hostname = "node3.mylab.local"
   node3.vm.network :private_network, ip: "192.168.56.13"
   end
   
   config.vm.define "node4" do |node4|
   node4.vm.box = "ubuntu/trusty64"
   node4.vm.hostname = "node4.mylab.local"
   node4.vm.network :private_network, ip: "192.168.56.14"
   end
   
   config.vm.define "tomcat" do |tomcat|
   tomcat.vm.box = "bento/centos-6.7"
   tomcat.vm.hostname = "tocat.mylab.local"
   tomcat.vm.network :private_network, ip: "192.168.56.15"
   end

   config.vm.define "apache" do |apache|
   apache.vm.box = "bento/centos-6.7"
   apache.vm.hostname = "apache.mylab.local"
   apache.vm.network :private_network, ip: "192.168.56.16"
   end
   config.vm.define "node5" do |node5|
   node5.vm.box = "bento/centos-6.7"
   node5.vm.hostname = "node5.mylab.local"
   node5.vm.network :private_network, ip: "192.168.56.17"
   config.vm.provision "shell", inline: <<-SHELL
   yum update

  SHELL
   end 
  

   config.vm.define "server6" do |server6|
   server6.vm.box = "centos/7"
   server6.vm.hostname = "server.raghu.com"
   server6.vm.network :private_network, ip: "192.168.56.20"
   config.vm.provision "shell", inline: <<-SHELL
    yum update
    yum install -y wget 
	yum install -y httpd
	service httpd start 
	chkconfig httpd on
	
  SHELL
  
  config.vm.provider "virtualbox" do |v|
  	v.memory = 2048
	v.cpus = 2
  end
end


 end
