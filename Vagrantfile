Vagrant.configure('2') do |config|
  config.vm.hostname = 'centos-9-stream'
  config.vm.box = 'alvistack/centos-9-stream'

  config.vm.provider :libvirt do |libvirt|
    libvirt.cpu_mode = 'host-passthrough'
    libvirt.cpus = 2
    libvirt.disk_bus = 'virtio'
    libvirt.disk_driver :cache => 'writeback'
    libvirt.driver = 'kvm'
    libvirt.memory = 8192
    libvirt.memorybacking :access, :mode => 'shared'
    libvirt.nested = true
    libvirt.nic_model_type = 'virtio'
    libvirt.storage :file, bus: 'virtio', cache: 'writeback'
    libvirt.video_type = 'virtio'
  end
end
