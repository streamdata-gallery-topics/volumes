---
swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 1
info:
  title: AWS OpsWorks API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeVolumes:
    get:
      summary: Describe Volumes
      description: Describes an instance's Amazon EBS volumes.
      operationId: describeVolumes
      x-api-path-slug: actiondescribevolumes-get
      parameters:
      - in: query
        name: InstanceId
        description: The instance ID
        type: string
      - in: query
        name: RaidArrayId
        description: The RAID array ID
        type: string
      - in: query
        name: StackId
        description: A stack ID
        type: string
      - in: query
        name: VolumeIds
        description: Am array of volume IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Describe
      - Volumes
---