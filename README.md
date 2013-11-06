packer-example-eu
-----------------

This is an example for using packer.io

The example on packer.io is outdated.

### Changes to the current example.json on packer.io

This is what I changed from the current (2013-11-06) example on http://www.packer.io/intro/getting-started/build-image.html

- use AWS Region 'eu-west-1' (Ireland)
- remove AWS credentials, so these are loaded from environment variables
- change Ubuntu image to latest Saucy micro AMI

### Setup

- packer is build on the Google Go language, so you have to install Go. On OSX: `$ brew install go`
- install packer from http://packer.io/ or in the command line on OSX `$ brew install packer`
- make sure you have an AWS account and AWS credentials set up 

#### AWS Credentials

You need to have set up your AWS Security Credentials from https://console.aws.amazon.com/iam/home?#security\_credential

Make sure to add them to your `~/.bash_profile` and run `$ source ~/.bash_profile`

### Building & Running

In case you set up properly and want to use same region and instance and source AMI

`$ packer verify example.json`

`$ packer build example.json`

