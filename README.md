# TF-AWS-VPC

# Terraform AWS VPC Module

This Terraform module creates a VPC with a public subnet in AWS.

## Usage

To use this module, include it in your Terraform configuration, specifying the required variables.

### Example

```hcl
module "vpc" {
  source = "github.com/Swanson-IT/TF-AWS-VPC?v1.0" # Use v1.0 tag

  name               = "my-vpc"                   # Desired name for the VPC and subnet
  vpc_cidr           = "10.0.0.0/16"              # CIDR block for the VPC
  public_subnet_cidr = "10.0.1.0/24"              # CIDR block for the public subnet
  availability_zone  = "us-west-2a"               # Availability zone for the public subnet
}