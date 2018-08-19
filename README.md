# aws
Commands to deploy--
## Cloudformation##
 aws cloudformation create-stack --template-body file://templates/single_instance_with_bastion_subnet.yml --stack-name single-instance-with-subnet --parameters ParameterKey=KeyName,ParameterValue=Bastion_instances ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyCidrIP,ParameterValue='***.***.***.***/32'

 aws cloudformation create-stack --template-body file://templates/Bastion_and_NAt.yml --stack-name Bastion-and-NAT-instances --parameters ParameterKey=KeyNameBastion,ParameterValue=Bastion_instances ParameterKey=KeyNameNat,ParameterValue=NAT_instances???? ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyCidrIP,ParameterValue='***.***.***.***/32'
  

MyCidrIP is your address IP which will be allowed by the EC2's specific security group.
