# AWS Quick Start for OpenVPN 

Deploy secure OpenVPN tunnel to an existing AWS VPC in 2 minutes.

Open source OpenVPN software. No license required. *Unlimited* simultaneous connections. Auto-generated config.

## Single click deploy to AWS regions

Click on the AWS QuicKstart URLs __below__ to deploy different AWS regions. They will open the AWS CloudFormnation stacks page, the you need just give a few options and start it.

### Europe

*Ireland:* [AWS: eu-west-1](https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*London:* [AWS: eu-west-2](https://console.aws.amazon.com/cloudformation/home?region=eu-west-2#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*Paris:* [AWS: eu-west-3](https://console.aws.amazon.com/cloudformation/home?region=eu-west-3#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)


*Frankfurt:* [AWS: eu-central-1](https://console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*Stockholm:* [AWS: eu-north-1](https://console.aws.amazon.com/cloudformation/home?region=eu-north-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

### North America

*US North Virginia:* [AWS: us-east-1](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*US Ohio:* [AWS: us-east-2](https://console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*US North California:* [AWS: us-west-1](https://console.aws.amazon.com/cloudformation/home?region=us-west-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*US Oregon:* [AWS: us-west-2](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*Canada Central:* [AWS: ca-central-1](https://console.aws.amazon.com/cloudformation/home?region=ca-central-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

### South America

*Sao Paulo:* [AWS: sa-east-1](https://console.aws.amazon.com/cloudformation/home?region=sa-east-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

### Asia Pacific, Australia, Japan

*Mumbai, India:* [AWS: ap-south-1](https://console.aws.amazon.com/cloudformation/home?region=ap-south-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*Seoul, South Korea:* [AWS: ap-northeast-2](https://console.aws.amazon.com/cloudformation/home?region=ap-northeast-2#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*Singapore:* [AWS: ap-southeast-1](https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*Sydney, Australia:* [AWS: ap-southeast-2](https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-2#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

*Tokyo, Japan:* [AWS: ap-northeast-1](https://console.aws.amazon.com/cloudformation/home?region=ap-northeast-1#/stacks/new?stackName=OpenVPN-Bastion&templateURL=https://s3-eu-west-1.amazonaws.com/tatobi-aws-quickstart-openvpn/cloudformation/ovpn-aws-deploy-vpc.yaml)

## Architecture

Here is an __example__ deployment architecture: where previously deployed EC2 instances running in multiple private subnets, and the public subnet deployed OpenVPN bastion provides accessibility through the secure VPN tunnel for the clients.

[![N|Solid](https://raw.githubusercontent.com/tatobi/aws-quickstart-openvpn/master/docs/architecture.png)](https://raw.githubusercontent.com/tatobi/aws-quickstart-openvpn/master/docs/architecture.png)

## Features

- very easy to deploy via AWS Quickstart URLs and AWS CloudFormation (__see below__),

- __one-click download openvpn config__ via an S3 signed URL (no need to SSH to host) from CloudFormation Output tab,

- __embedded vpn config__ file: contains everything you need, muliple config file created at once (up to 100),

- tested on: __Windows 10, Linux (Ubuntu), Android, Mac OSX (tunnelblick)__,

- __secure:__ SHA512 channel auth, AES-256-CBC encryption, TLS 1.2 forced (openvpn > v2.3.10  or higher client versions needed!), __NO SSH__, access instance via AWS SSM,

- __traffic routing options:__ __gateway/TCP443 (HTTPS)__ or VPC only/UDP443,

- __anonymous:__ no VPN log files on servers, use local+AWS DNS server forced through the tunnel,

- __fast caching DNS:__ caching dnsmasq installed and used on server side, pushed to VPN client,


- seamless teardown with AWS Lambda,

- __ALL AWS regions supported__ by dynamic AMI selection with AWS Lambda,

- based on __Ubuntu 18.04LTS__ latest version.


## Prerequisities

You need an AWS account and  full EC2 and IAM rights.


## AWS CloudFormation parameters


__Stack Name:__ choose a sdtack name (QS default: OpenVPN-Bastion),

__VPC ID:__ choose an existing VPC where the OpenVPN instance going to be deployed,

__VPC Public Subnet:__ choose a __*public*__ subnet within the VPC above (public is important, otherwise the bastion won't be accessible),

__Limit external access to CIDR:__ optional, you can limite which IPs can connect to the bastion, 0.0.0.0/0 accessible from everywhere,

__AWS EC2 Instance Type:__ choose an instance type from t2 and t3 Ec2 calsses (t2.micro is default because it is eligible for __FREE TIER__),

__The number of generated OpenVPN connection profiles:__ how many openvpn config will be generated, multiple one means many hosts can use simultaneously the VPN conection (default: 10, max: 200),

__Traffic routing:__ choose you ALL traffic, including the VPC and public Internet, (default gateway mode) __*ALL_GATEWAY_TCP443*__ routed through the tunnel, OR only the AWS VPC internal traffic: __*VPC_ONLY_UDP443*__. 

__IMPORTANT:__ in ALL_GATEWAY_TCP443 everything is going throug the VPN, it can be slower for remote desktop connections, but suitable for secure VPN tunnel from public places like a Hotel, hotspot, airport, etc...

__Cloudformation Steps:__

1. Choose a link above, click "Next",

2. Fill CloudFormation parameters, then Click "Next",

3. Click "Next",

4. Scroll down, check checkbox: "I acknowledge that AWS CloudFormation might create IAM resources."

5. Click "Create"


Then wait the stack to be __GREEN__ status: __CREATE_COMPLETE__.

## Client connection

After the stack completd, download the OpenVPN config profile __ZIP file__ by the S3 URL you can find below the CloudFormation stack's __Outputs__ tab.

__DownloadOpenVPNProfilesURL__: [S3 signed URL](https://s3.signed.url/)

Copy the URL to tyour browser and download the file.

__IMPORTANT:__ by default the link is available for 12 hours after creation, for securiry reasons.

__NOTE on Windows 10:__ ZIP files does not work natively anymnore, Microsoft baffted handling them correctly (not the ZIp files invalid!), I recommend download and install the Open Source alternative: [7-ZIP](https://www.7-zip.org/) or __WinZIP__ to extract the config files.

__UNZIP__ the downloaded ZIP file and save the *.ovpn files to a folder. __*Pick a one, or share with other devices to connect.*__

### Clients

__Linux:__

```
openvpn --config *.ovpn

```
__Windows:__

1. [Install OpenVPN GUI](https://openvpn.net/community-downloads/)

2. Start it

3. Open systray icon with right click, Import files.., add *.ovpn confiog files and connect it. 

__MAC OSX:__

[Install Tunnelblick](https://tunnelblick.net/cInstall.html)

__Android:__

[OpenVPN for Androind](https://play.google.com/store/apps/details?id=net.openvpn.openvpn)

Open app, import profile, import the *.ovpn file.

## Tear down

Simple delete the AWS CloudFormation stack. It will delete the S3 config folder with the openvpn configuration files as well.


## Need more client certificate? Revoke existing?

You can connect to the OpenVPN EC2 instance console, using the AWS SSM Session manager (WEB or CLI) to have a remote console.

[AWS SSM session manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager-working-with-sessions-start.html#start-sys-console)

Go to:

__OpenVPN base path:__ /etc/openvpn/keygen/

__Generate certificates:__

[OpenVPN commands](keygen/README.md)


__Download fenerated keys:__ /etc/openvpn/keys/{config_name}


## Documentation

- [AWS CloudFormation](https://aws.amazon.com/cloudformation/getting-started/)

- [OpenVPN WIKI](https://community.openvpn.net/openvpn/wiki)

- [OpenVPN Source Code](https://github.com/OpenVPN)

- [OpenVPN Hardening](https://community.openvpn.net/openvpn/wiki/Hardening)

## License

All of here is open source software, licensed under Apache 2.0 license.



















