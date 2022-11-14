# terraform-aws-ec2-scheduler

This is a module to create a schedule to shut down or start a EC2 Instance.

The following resources will be created:
 - AWS Cloudwatch event rule - Delivers a real-time stream of system events that shut down or start the EC2.
 - Identity Access Management (IAM) that create a service role for Systems Manager Automation

<!--- BEGIN_TF_DOCS --->

## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12.0 |

## Providers

| Name | Version |
|------|---------|
| aws | n/a |
| random | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| cron\_start | Cron expression to define when to trigger a start of the EC2 | `any` | n/a | yes |
| cron\_stop | Cron expression to define when to trigger a stop of the EC2 | `any` | n/a | yes |
| enable | n/a | `bool` | `true` | no |
| instanceid | EC2 instance id for schedule | `any` | n/a | yes |

## Outputs

No output.

<!--- END_TF_DOCS --->
