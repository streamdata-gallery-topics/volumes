---
swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 0
info:
  title: AWS OpsWorks API Assign Volume
  version: 1.0.0
  description: Assigns one of the stack's registered Amazon EBS volumes to a specified
    instance.
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