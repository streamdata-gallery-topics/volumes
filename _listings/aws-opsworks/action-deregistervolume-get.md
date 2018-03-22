---
swagger: "2.0"
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
  /?Action=DeregisterVolume:
    get:
      summary: ' Deregister Volume '
      description: Deregisters an Amazon EBS volume
      operationId: deregisterVolume
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
      - volumes
definitions: []
x-collection-name: AWS OpsWorks
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