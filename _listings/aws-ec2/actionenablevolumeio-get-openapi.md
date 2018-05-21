---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Enable Volume I O
  version: 1.0.0
  description: |-
    Enables I/O operations for a volume that had I/O operations disabled because the data on the
          volume was potentially inconsistent.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeVolumeAttribute:
    get:
      summary: Describe Volume Attribute
      description: Describes the specified attribute of the specified volume.
      operationId: describevolumeattribute
      x-api-path-slug: actiondescribevolumeattribute-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of volume results returned by DescribeVolumes
          in paginated      output
        type: string
      - in: query
        name: NextToken
        description: The NextToken value returned from a previous paginated        DescribeVolumes
          request where MaxResults was used and the results      exceeded the value
          of that parameter
        type: string
      - in: query
        name: VolumeId.N
        description: One or more volume IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=DescribeVolumes:
    get:
      summary: Describe Volumes
      description: Describes the specified EBS volumes.
      operationId: describevolumes
      x-api-path-slug: actiondescribevolumes-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of volume results returned by DescribeVolumeStatus
          in      paginated output
        type: string
      - in: query
        name: NextToken
        description: The NextToken value to include in a future DescribeVolumeStatus      request
        type: string
      - in: query
        name: VolumeId.N
        description: One or more volume IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=EnableVolumeIO:
    get:
      summary: Enable Volume I O
      description: |-
        Enables I/O operations for a volume that had I/O operations disabled because the data on the
              volume was potentially inconsistent.
      operationId: enablevolumeio
      x-api-path-slug: actionenablevolumeio-get
      parameters:
      - in: query
        name: Attribute
        description: The snapshot attribute to modify
        type: string
      - in: query
        name: CreateVolumePermission
        description: A JSON representation of the snapshot attribute modification
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: OperationType
        description: The type of operation to perform to the attribute
        type: string
      - in: query
        name: SnapshotId
        description: The ID of the snapshot
        type: string
      - in: query
        name: UserGroup.N
        description: The group to modify for the snapshot
        type: string
      - in: query
        name: UserId.N
        description: The account ID to modify for the snapshot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---