# Terraform-EC2-Deployment
# 🚀 Deploy your first EC2 using terraform

# Step 1 
Install [Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli), [awscli](https://docs.aws.https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.htmlamazon.com/cli/latest/userguide/getting-started-install.html) and [VSCode](https://code.visualstudio.com/)

# step 2 VSCODE extensions
 Open VSCODE and Install Terraform Extension (I already have my installed)
 #
![vscode_extensions_install](https://github.com/user-attachments/assets/4bdfbef1-4858-4c9d-aa92-b9c374425a32)

# Step 3 IAM User
Create a [IAM user](https://guide.sst.dev/chapters/create-an-iam-user.html)
and save the Secret access key
# Step 4 Authentication
There is many ways to Authenticate, but for this project we will use "aws configure" method. On windows "CMD" and Unix systems "Terminal". You can also use the terminal inside VSCODE which makes things easier. To do so, click on the top left where you see "Terminal" and select "New Terminal". You should have a new open Terminal in the bottom where you can write the commands as showing:
```sh
aws configure
```
You will be ask for the Access Key, Secret Key and default region from >> Step 3 <<
#
![aws_configure](https://github.com/user-attachments/assets/eeeff569-8883-45a1-b907-675cf37b1da2)

The AWS Provider can source credentials and other settings from the shared configuration and credentials files. By default, these files are located at $HOME/.aws/config and $HOME/.aws/credentials on Linux and macOS, and "%USERPROFILE%\.aws\config" and "%USERPROFILE%\.aws\credentials" on Windows.

# Note!!! 
To build are first EC2 with terrafomr we will need a provider and the resource 
#
# For your understanding
Resources are a fundamental element of the Terraform language. They are components within a Terraform configuration that define infrastructure objects or services to be managed, such as an EC2 instance. On the other hand, providers are plugins that enable interaction with different infrastructure services and platforms. 

# Step 5 Create project folder
Create a Folder and name it EC2. Open VSCODE and click on "File>Open Folder" and find the folder you have just created. Once you are inside the folder click on the "File" icon to create a new file and name it "myfirstec2.tf". Do not forget the ".tf" at the end!!!
![VSCODE_new_file](https://github.com/user-attachments/assets/ac35e611-1e99-4654-9839-d58c9f3609ce)

# Step 6 EC2 infrastructure 
After creating the "myfirstec2.tf" file, you should be able to write your first terraform code in the right. Copy and paste:
```sh
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "web" {
  ami           = "ami-0e2c8caa4b6378d8c"
  instance_type = "t2.micro"

  tags = {
    Name = "MyfirstEC2"
  }
}
```
# For your understanding
I will brake down the code to explain.
```sh

provider "aws"                  is the plugin for the infrastructure
region = "us-east-1"            is well... the region for the infrastructure that we are building
resource "aws_instance" "web"   is the resouce (ec2) that we are building with the name "web"
ami  = "ami-0e2c8caa4b6378d8c"  is the Amazon Machine Image (ami) ID. This is the OS that we are choosing for our ec2 intance
instance_type = "t2.micro"      is the hardware type we are choosing like CPU, memory, storage, and networking capacity

tags = {
Name = "MyfirstEC2"             is the name of our ec2 instance 




