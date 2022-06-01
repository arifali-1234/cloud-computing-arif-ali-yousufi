# cloud-computing-arif-ali-yousufi
assinment of cloud to ec2 and s3 bucket in the terraform
for this proccessing of my assignment i have 3 folder by the nameo 
lab 01 {which is the definted the main resources)
lab 01 {which is to defined the main resources, the variable and linked bettween main resource and the variable}

lab 03 {which is to defined the state of bucket,ec2 in the terraform ,s3 in terraform and how we change the state } 

at the durition of my price i don't more like three option and i know about the uses of 
terraform init {C:\Users\Administrator\Desktop\03\.terraform\providers\registry.terraform.io\hashicorp\aws\4.16.0\windows_amd64\terraform-provider-aws_v4.16.0_x5.exe}
terraform plan {C:\Users\Administrator\Desktop\03\.terraform.lock.hcl}
terraform apply {C:\Users\Administrator\Desktop\03\.terraform\terraform.tfstate}
this code which i content in the below of progaraph that shows the summry of my working 
in which region .......

provider "aws" {
  region = "us-west-2"
}

resource "aws_s3_bucket" "main_s3_bucket" {
  bucket = "my-arif-ali-2022"
  tags = {
    Name        = "My bucket"
    Environment = "Dev"
  }
}
    


resource "aws_instance" "app_server" {
  ami           = "ami-08d70e59c07c61a3a"
  instance_type = "t2.micro"
  tags = {
    Name = var.arif_ali
  }
}

terraform {
    backend "s3"{
       bucket ="my-arif-ali-2022"
      key = "terraform-state.state"
      region = "us-west-2"
      }
     
    }

this is my short descrition about work all of these process
thank you for these project i hope which our have more of assignment in the future 



because of these assignment i don't sleeping good in the last weekend.
