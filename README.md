# Terraform-EC2-Deployment
# 🚀 Deploy your first EC2 using terraform

# Step 1 
Install [Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli), [awscli](https://docs.aws.https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.htmlamazon.com/cli/latest/userguide/getting-started-install.html) and [VSCode](https://code.visualstudio.com/)

# step 2 VSCode extensions
 Open VSCode and Install Terraform Extension (I already have my installed)
 #
![vscode_extensions_install](https://github.com/user-attachments/assets/4bdfbef1-4858-4c9d-aa92-b9c374425a32)

# Step 3 IAM user
Create a [IAM user](https://guide.sst.dev/chapters/create-an-iam-user.html)
and save the Secret access key
# Step 4 Authentication
There is many ways to Authenticate, but for this project we will use "aws configure" method. On windows "CMD" and Unix systems "Terminal". You can also use the terminal inside VSCode which makes things easier. To do so, click on the top left where you see "Terminal" and select "New Terminal". You should have a new open Terminal in the bottom where you can write the commands as showing:
```sh
aws configure
```
You will be ask for the Access Key, Secret Key and default region from >> Step 3 <<
#
![aws_configure](https://github.com/user-attachments/assets/eeeff569-8883-45a1-b907-675cf37b1da2)

The AWS Provider can source credentials and other settings from the shared configuration and credentials files. By default, these files are located at $HOME/.aws/config and $HOME/.aws/credentials on Linux and macOS, and "%USERPROFILE%\.aws\config" and "%USERPROFILE%\.aws\credentials" on Windows.
