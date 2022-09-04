Vagrant.configure("2") do |config|
  # config.vm.provision "shell", inline: "echo Hello"
  config.vm.provision "shell", inline: <<-SHELL
    export DEBIAN_FRONTEND=noninteractive
    useradd --create-home --password "a.RYSPY0uUhkw" --shell /bin/bash user
    SHELL
  config.vm.box = "generic/ubuntu2004"
  config.vm.provider "virtualbox" do |v|
    v.gui = true
  end

  config.vm.define "lbl1" do |lbl1|
    lbl1.vm.hostname = "lbl1"
    lbl1.vm.network "public_network", ip: "192.168.1.131"
  end

  config.vm.define "lbl2" do |lbl2|
    lbl2.vm.hostname = "lbl2"
    lbl2.vm.network "public_network", ip: "192.168.1.132"
  end

  config.vm.define "app1" do |app1|
    app1.vm.hostname = "app1"
    app1.vm.network "public_network", ip: "192.168.1.141"
  end

  config.vm.define "app2" do |app2|
    app2.vm.hostname = "app2"
    app2.vm.network "public_network", ip: "192.168.1.142"
  end

  config.vm.define "app3" do |app3|
    app3.vm.hostname = "app3"
    app3.vm.network "public_network", ip: "192.168.1.143"
  end

  config.vm.define "wrk1" do |wrk1|
    wrk1.vm.hostname = "wrk1"
    wrk1.vm.network "public_network", ip: "192.168.1.151"
  end

  config.vm.define "sbl1" do |sbl1|
    sbl1.vm.hostname = "sbl1"
    sbl1.vm.network "public_network", ip: "192.168.1.161"
  end

  config.vm.define "sbl2" do |sbl2|
    sbl2.vm.hostname = "sbl2"
    sbl2.vm.network "public_network", ip: "192.168.1.162"
  end

  config.vm.define "dba1" do |dba1|
    dba1.vm.hostname = "dba1"
    dba1.vm.network "public_network", ip: "192.168.1.171"
  end

  config.vm.define "dba2" do |dba2|
    dba2.vm.hostname = "dba2"
    dba2.vm.network "public_network", ip: "192.168.1.172"
  end

  config.vm.define "dba3" do |dba3|
    dba3.vm.hostname = "dba3"
    dba3.vm.network "public_network", ip: "192.168.1.173"
  end

  config.vm.define "sto1" do |sto1|
    sto1.vm.hostname = "sto1"
    sto1.vm.network "public_network", ip: "192.168.1.181"
  end

  config.vm.define "dbr1" do |dbr1|
    dbr1.vm.hostname = "dbr1"
    dbr1.vm.network "public_network", ip: "192.168.1.191"
  end

end