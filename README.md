## Infrastructure as Code with AWS Cloud Formation
 First step is to have an AWS account,aws cli for configuring access key.
## Steps To implement

* Creating private subnets for RDS - These act as the infrastucture, and the cloud formation stack be created first. 
* Creating DB Security Group
* S3 Bucket creation
* RDS instance - Since database are created for a one time use,created its specific stack in the rdstemplate.yml file
* User Data
* IAM Policy - For the IAM Policy,Userdata and IAM role this are included in the server.yml file
* IAM Role


## Deploying stacks format:

### To create infrastructure you run command:

```
./create.sh infrastack infra.yml infra-parameters.json
```

### To create server you run command:

```
./create.sh ourdemoservers servers.yml server-parameters.json
```

### For RDS cloudformation template run:
```
./create.sh ourdemoservers rdstemplate.yml rdsparameters.json
```

### To create s3 bucket via the template you run command

```
./create.sh bucketstack bucket.yml 
```
Note: Rem to remove the second parameter in the create.sh as this file doe not contain.json file. This helps avoid errors while creating stack.
