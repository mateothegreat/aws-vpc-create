# Create AWS VPC

Features:

* Creates (optional) peering connection(s).
* Supports tagging for ALL resources.


This role will create a new AWS VPC including:

* Peering Connection(s)
* Internet Gateway
* NAT Gateway(s)
* Route Table(s)
* Subnet(s)



## Requirements

```bash
pip install ansible boto3 boto
```
## Variables

```yaml
redis:
  bind: "0.0.0.0"
  port: "6379"
```

## Example Usage

Add the following to a file like `playbook.yaml`:

```yaml
- hosts: monitoring
  roles:
    - role: "mateothegreat.redis_latest"
      vars:
        redis:
          bind: "0.0.0.0"
          port: "6379"
```

Run with `ansible-playbook -i <your inventory file> playbook.yaml`.
