Vagrant.configure("2") do |config|
  config.vm.define 'ubuntu1604-amd64' do |instance|
    instance.vm.box = 'ubuntu/xenial64'

    config.vm.provision "shell" do |s|
      s.inline = "sudo apt-get install -y python"
    end

    config.vm.provision "ansible" do |ansible|
      ansible.playbook = 'test.yml'
      ansible.verbose = 'vv'
      ansible.sudo = true
    end
  end
end
