---
name: AWS OpsWorks
x-slug: aws-opsworks
description: AWS OpsWorks is a configuration management service that uses Chef, an
  automation platform that treats server configurations as code. OpsWorks uses Chef
  to automate how servers are configured, deployed, and managed across your Amazon
  Elastic Compute Cloud (Amazon EC2) instances or on-premises compute environments.
  OpsWorks has two offerings, AWS Opsworks for Chef Automate, and AWS OpsWorks Stacks.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
x-kinRank: "10"
x-alexaRank: ""
tags: Volumes
created: "2018-05-20"
modified: "2018-05-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/apis.md
specificationVersion: "0.14"
apis:
- name: AWS OpsWorks API Assign Volume
  x-api-slug: aws-opsworks-api
  description: Assigns one of the stack's registered Amazon EBS volumes to a specified
    instance.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
  humanURL: https://aws.amazon.com/opsworks/
  baseURL: ://///?Action=AssignVolume
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/actionassignvolume-get-openapi.md
- name: AWS OpsWorks API Deregister Volume
  x-api-slug: aws-opsworks-api
  description: Deregisters an Amazon EBS volume.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
  humanURL: https://aws.amazon.com/opsworks/
  baseURL: ://///?Action=DeregisterVolume
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/actionderegistervolume-get-openapi.md
- name: AWS OpsWorks API Describe Volumes
  x-api-slug: aws-opsworks-api
  description: Describes an instance's Amazon EBS volumes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
  humanURL: https://aws.amazon.com/opsworks/
  baseURL: ://///?Action=DescribeVolumes
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/actiondescribevolumes-get-openapi.md
- name: AWS OpsWorks API Register Volume
  x-api-slug: aws-opsworks-api
  description: Registers an Amazon EBS volume with a specified stack.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
  humanURL: https://aws.amazon.com/opsworks/
  baseURL: ://///?Action=RegisterVolume
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/actionregistervolume-get-openapi.md
- name: AWS OpsWorks API Unassign Volume
  x-api-slug: aws-opsworks-api
  description: Unassigns an assigned Amazon EBS volume.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
  humanURL: https://aws.amazon.com/opsworks/
  baseURL: ://///?Action=UnassignVolume
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/actionunassignvolume-get-openapi.md
- name: AWS OpsWorks API Update Volume
  x-api-slug: aws-opsworks-api
  description: Updates an Amazon EBS volume's name or mount point.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
  humanURL: https://aws.amazon.com/opsworks/
  baseURL: ://///?Action=UpdateVolume
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/actionupdatevolume-get-openapi.md
- name: AWS OpsWorks API
  x-api-slug: aws-opsworks-api
  description: AWS OpsWorks is a configuration management service that uses Chef,
    an automation platform that treats server configurations as code. OpsWorks uses
    Chef to automate how servers are configured, deployed, and managed across your
    Amazon Elastic Compute Cloud (Amazon EC2) instances or on-premises compute environments.
    OpsWorks has two offerings, AWS Opsworks for Chef Automate, and AWS OpsWorks Stacks.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Management-Tools_AWSOpsWorks.png
  humanURL: https://aws.amazon.com/opsworks/
  baseURL: :///
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-opsworks/openapi.md
x-common:
- type: x-command-line-interface
  url: http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html
- type: x-documentation
  url: http://docs.aws.amazon.com/opsworks/latest/APIReference/Welcome.html
- type: x-website
  url: https://aws.amazon.com/opsworks/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---