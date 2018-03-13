---
swagger: "2.0"
info:
  title: AWS Storage Gateway Service API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListVolumes&k=1:
    get:
      summary: ' List Volumes '
      description: Lists the iSCSI stored volumes of a gateway
      operationId: listVolumes
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      - in: query
        name: Limit
        description: Specifies that the list of volumes returned be limited to the
          specified number of         items
        type: string
      - in: query
        name: Marker
        description: A string that indicates the position at which to begin the returned
          list of volumes
        type: string
      responses:
        200:
          description: OK
      tags:
      - volumes
definitions: []
x-collection-name: AWS Storage Gateway Service
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