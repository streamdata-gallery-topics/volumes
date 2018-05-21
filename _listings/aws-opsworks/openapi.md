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
  /?Action=AssignVolume:
    get:
      summary: Assign Volume
      description: Assigns one of the stack's registered Amazon EBS volumes to a specified
        instance.
      operationId: assignVolume
      x-api-path-slug: actionassignvolume-get
      parameters:
      - in: query
        name: InstanceId
        description: The instance ID
        type: string
      - in: query
        name: VolumeId
        description: The volume ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=DeregisterVolume:
    get:
      summary: Deregister Volume
      description: Deregisters an Amazon EBS volume.
      operationId: deregisterVolume
      x-api-path-slug: actionderegistervolume-get
      parameters:
      - in: query
        name: VolumeId
        description: The AWS OpsWorks Stacks volume ID, which is the GUID that AWS
          OpsWorks Stacks assigned to the instance when you registered the volume
          with the stack, not the Amazon EC2 volume ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
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
      - Volumes
  /?Action=RegisterVolume:
    get:
      summary: Register Volume
      description: Registers an Amazon EBS volume with a specified stack.
      operationId: registerVolume
      x-api-path-slug: actionregistervolume-get
      parameters:
      - in: query
        name: Ec2VolumeId
        description: The Amazon EBS volume ID
        type: string
      - in: query
        name: StackId
        description: The stack ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=UnassignVolume:
    get:
      summary: Unassign Volume
      description: Unassigns an assigned Amazon EBS volume.
      operationId: unassignVolume
      x-api-path-slug: actionunassignvolume-get
      parameters:
      - in: query
        name: VolumeId
        description: The volume ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=UpdateVolume:
    get:
      summary: Update Volume
      description: Updates an Amazon EBS volume's name or mount point.
      operationId: updateVolume
      x-api-path-slug: actionupdatevolume-get
      parameters:
      - in: query
        name: MountPoint
        description: The new mount point
        type: string
      - in: query
        name: Name
        description: The new name
        type: string
      - in: query
        name: VolumeId
        description: The volume ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
---