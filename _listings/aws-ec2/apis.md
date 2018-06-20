---
name: AWS EC2
x-slug: aws-ec2
description: Amazon Elastic Compute Cloud is a web service that provides resizable
  compute capacity in the cloud. It is designed to make web-scale cloud computing
  easier for developers. Amazon EC2s simple web service interface allows you to obtain
  and configure capacity with minimal friction. It provides you with complete control
  of your computing resources and lets you run on Amazon&rsquo;s proven computing
  environment. Amazon EC2 reduces the time required to obtain and boot new server
  instances to minutes, allowing you to quickly scale capacity, both up and down,
  as your computing requirements change. Amazon EC2 changes the economics of computing
  by allowing you to pay only for capacity that you actually use. Amazon EC2 provides
  developers the tools to build failure resilient applications and isolate themselves
  from common failure scenarios.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Volumes
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/apis.md
specificationVersion: "0.14"
apis:
- name: AWS EC2 API Describe Volume Attribute
  x-api-slug: aws-ec2-api
  description: Describes the specified attribute of the specified volume.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
  humanURL: https://aws.amazon.com/ec2/
  baseURL: ://///?Action=DescribeVolumeAttribute
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/actiondescribevolumeattribute-get-openapi.md
- name: AWS EC2 API Describe Volumes
  x-api-slug: aws-ec2-api
  description: Describes the specified EBS volumes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
  humanURL: https://aws.amazon.com/ec2/
  baseURL: ://///?Action=DescribeVolumes
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/actiondescribevolumes-get-openapi.md
- name: AWS EC2 API Enable Volume I O
  x-api-slug: aws-ec2-api
  description: |-
    Enables I/O operations for a volume that had I/O operations disabled because the data on the
          volume was potentially inconsistent.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
  humanURL: https://aws.amazon.com/ec2/
  baseURL: ://///?Action=EnableVolumeIO
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/actionenablevolumeio-get-openapi.md
- name: AWS EC2 API
  x-api-slug: aws-ec2-api
  description: Amazon Elastic Compute Cloud is a web service that provides resizable
    compute capacity in the cloud. It is designed to make web-scale cloud computing
    easier for developers. Amazon EC2s simple web service interface allows you to
    obtain and configure capacity with minimal friction. It provides you with complete
    control of your computing resources and lets you run on Amazon&rsquo;s proven
    computing environment. Amazon EC2 reduces the time required to obtain and boot
    new server instances to minutes, allowing you to quickly scale capacity, both
    up and down, as your computing requirements change. Amazon EC2 changes the economics
    of computing by allowing you to pay only for capacity that you actually use. Amazon
    EC2 provides developers the tools to build failure resilient applications and
    isolate themselves from common failure scenarios.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonEC2.png
  humanURL: https://aws.amazon.com/ec2/
  baseURL: :///
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/aws-ec2/openapi.md
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
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---