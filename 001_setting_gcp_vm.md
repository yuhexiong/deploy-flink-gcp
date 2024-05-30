# Setting GCP VM

## GCP VM Instances Page

- click 'CREATE INSTANCES'
![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/001_vm_instances_page.png)

## Setting VM Information

- Name: (whatever you like)
- Region: asia-east1(Taiwan), Zone: a/b/c all ok
- Machice: E2, Machice Type: e2-standard-4(4 vCPU, 2 core, 16 GB memory) (choose your own settings)

![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/002_create_vm_page.png)

- Boot Disk Operating system: Ubuntu (will affect subsequent startup instructions)
- Boot Disk Name: (whatever you like)
- Boot Disk Size: 30 (choose your own settings)
![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/003_create_vm_page_boot_disk.png)

- Networking tags: two tags, one for ssh port 22, one for flink port 8081(whatever you like but same as the firewall target tags set later)
![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/004_create_vm_page_advenced_network_tags.png)

- Networking interface: gke-network
- Networking interface Subnetwork: subnet-asia-east1 IPv4(10.1.0.0/16)
![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/005_create_vm_page_advenced_network_interfaces.png)

## Click 'CREATE'