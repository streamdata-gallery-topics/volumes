---
swagger: "2.0"
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
  /?Action=EnableVolumeIO:
    get:
      summary: Enable Volume I O
      description: |-
        Enables I/O operations for a volume that had I/O operations disabled because the data on the
              volume was potentially inconsistent
      operationId: enablevolumeio
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
      - volumes
definitions: []
x-collection-name: AWS EC2
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