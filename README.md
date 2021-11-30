# opensearch-terraform

- Please configure the aws cli using ```aws configure```

- Please change the region in provider accordingly

- Please chnage the subnet id in main.tf


Apply the below commands


```
terraform init

terraform validate

terraform apply

```

Once the cluster is up and green, to test it you need to create ec2 instance in the same vpc and subnet.


- After creating the ec2, apply the below command to test the opensearch cluster.


```ssh -i opensearch.pem ec2-user@ec2-65-2-129-103.ap-south-1.compute.amazonaws.com -N -L 9200:vpc-dkes-y5tqz5op74qluchzfzrqkdib5e.ap-south-1.es.amazonaws.com:443```



- Note: 

```

where opensearch.pem is my ssh key

where ec2-user@ec2-65-2-129-103.ap-south-1.compute.amazonaws.com is my instance domain

where vpc-dkes-y5tqz5op74qluchzfzrqkdib5e.ap-south-1.es.amazonaws.com is my vpc endpoint

```


```
For the security group, specify two inbound rules:

add 22 and 443 rules
```
