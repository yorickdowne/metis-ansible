# Deploy RPC with Ansible

## System requirement

- Linux(x86_64)
- docker
- Ethereum node with full history
- Ansible 9 and Python 3.12

## Andromeda

### Recommened hardware

1. AWS c5.2xlarge with ipv4 network
2. 500Gb ebs gp3 with 200 throughput
3. open 30303 tcp/udp for p2p connnections

### Steps

3. update `hosts.ini` file, add your remote ip and eth mainnet rpc endpoint there
4. install docker and docker-compose by `ansible-playbook playbooks/docker.yaml`
5. spin up your andromeda rpc by `ansible-playbook playbooks/andromeda.yaml`
6. install docker-autoheal by `ansible-playbook playbooks/autoheal.yaml`

### snapshots

We provided public aws ebs snapshot for you if you need them.

l2geth

snap-0cffd87f09b9a723d

l1dtl

snap-040379f7ef7beb2c0

You can use the snapshots on aws **us-east-2** region, and copy them to another region you are using.

## Sepolia

### Recommened hardware

1. AWS c5.xlarge with ipv4 network
2. 50Gb free disk
3. open 30303 tcp/udp for p2p connnections

### Steps

3. update `hosts.ini` file, add your remote ip and eth sepolia rpc endpoint there
4. install docker and docker-compose by `ansible-playbook playbooks/docker.yaml`
5. spin up your sepolia rpc by `ansible-playbook playbooks/sepolia.yaml`
6. install docker-autoheal by `ansible-playbook playbooks/autoheal.yaml`

### Snapshot

We provided public aws ebs snapshot for you if you need them.

l2geth

snap-07ed6398665bf62da

l1dtl

vol-02478ee8fbc049106

You can use the snapshots on aws **us-east-1** region, and copy them to another region you are using.
