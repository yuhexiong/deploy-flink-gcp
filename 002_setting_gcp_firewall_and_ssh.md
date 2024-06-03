# Setting GCP Firewall And SSH

## GCP Firewall Policies Page

- click 'CREATE FIREWALL RULE'
![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/006_firewall_policies_page.png)

## Setting Firewall Rule

- Use same steps to create ssh firewall rule for port 22
- Name: (whatever you like)
- Network: gke-network
- Target tags: (same as tag used in VM)
- Source filter: IPv4 ranges
- Source IPv4 ranges: (your own IP)

![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/007_create_firewall_rule_page_v2.png)

- Protocols and ports TCP: 8081

![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/008_create_firewall_rule_page_port.png)

- click 'CREATE'

## Setting SSH

- Generate key on your computer
- Metadata SSH KEYS Page add your public key

![image](https://github.com/yuhexiong/deploy-flink-gcp/blob/main/image/009_metadata_ssh_keys_v2.png)

## SSH VM

- use a normal terminal to enter the gcp virtual instance
```
ssh -i ${ssh private key path} ${metadata-username}@${vm External IP address}
```