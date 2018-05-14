---
name: AWS EC2
description: Amazon Elastic Compute Cloud is a web service that provides resizable
  compute capacity in the cloud. It is designed to make web-scale cloud computing
  easier for developers. Amazon EC2s simple web service interface allows you to obtain
  and configure capacity with minimal friction. It provides you with complete control
  of your computing resources and lets you run on Amazonrsquo;s proven computing environment.
  Amazon EC2 reduces the time required to obtain and boot new server instances to
  minutes, allowing you to quickly scale capacity, both up and down, as your computing
  requirements change. Amazon EC2 changes the economics of computing by allowing you
  to pay only for capacity that you actually use. Amazon EC2 provides developers the
  tools to build failure resilient applications and isolate themselves from common
  failure scenarios.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
x-kinRank: "10"
x-alexaRank: ""
tags:
- Stack Network
- Stack
- Compute
- Amazon Web Services
created: "2018-03-24"
modified: "2018-03-24"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/apis.yaml
specificationVersion: "0.14"
apis:
- name: AWS EC2 API
  description: Amazon Elastic Compute Cloud is a web service that provides resizable
    compute capacity in the cloud
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
  humanURL: ""
  baseURL: :///
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/action-enablevolumeio-get.md
- name: AWS EC2 API Describe Volumes
  description: Describes the specified EBS volumes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
  humanURL: https://aws.amazon.com/ec2/
  baseURL: http:://{host}//
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/action-describevolumes-get.md
x-common:
- type: x-code
  url: http://aws.amazon.com/code/Amazon-EC2/
- type: x-documentation
  url: http://docs.aws.amazon.com/AWSEC2/latest/APIReference/Welcome.html
- type: x-faq
  url: https://aws.amazon.com/ec2/faqs/
- type: x-getting-started
  url: https://aws.amazon.com/ec2/getting-started/
- type: x-pricing
  url: https://aws.amazon.com/ec2/pricing/
- type: x-sla
  url: https://aws.amazon.com/ec2/sla/
- type: x-website
  url: https://aws.amazon.com/ec2/
- type: x-code
  url: http://aws.amazon.com/code/Amazon-EC2/
- type: x-documentation
  url: http://docs.aws.amazon.com/AWSEC2/latest/APIReference/Welcome.html
- type: x-faq
  url: https://aws.amazon.com/ec2/faqs/
- type: x-getting-started
  url: https://aws.amazon.com/ec2/getting-started/
- type: x-pricing
  url: https://aws.amazon.com/ec2/pricing/
- type: x-sla
  url: https://aws.amazon.com/ec2/sla/
- type: x-website
  url: https://aws.amazon.com/ec2/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---