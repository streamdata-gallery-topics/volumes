---
swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 0
info:
  title: AWS Storage Gateway Service API List Volumes
  version: 1.0.0
  description: Lists the iSCSI stored volumes of a gateway.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteVolume:
    get:
      summary: Delete Volume
      description: Deletes the specified gateway volume that you previously created
        using the.
      operationId: deleteVolume
      x-api-path-slug: actiondeletevolume-get
      parameters:
      - in: query
        name: VolumeARN
        description: The Amazon Resource Name (ARN) of the volume
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=DescribeCachediSCSIVolumes:
    get:
      summary: Describe Cached SCSI Volumes
      description: Returns a description of the gateway volumes specified in the request.
      operationId: describeCachediSCSIVolumes
      x-api-path-slug: actiondescribecachediscsivolumes-get
      parameters:
      - in: query
        name: VolumeARNs
        description: 'Type: array of Strings'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cached SCSI Volumes
  /?Action=DescribeStorediSCSIVolumes:
    get:
      summary: Describe Stored SCSI Volumes
      description: Returns the description of the gateway volumes specified in the
        request.
      operationId: describeStorediSCSIVolumes
      x-api-path-slug: actiondescribestorediscsivolumes-get
      parameters:
      - in: query
        name: VolumeARNs
        description: An array of strings where each string represents the Amazon Resource
          Name (ARN) of a         stored volume
        type: string
      responses:
        200:
          description: OK
      tags:
      - Stored SCSI Volumes
  /?Action=ListVolumes:
    get:
      summary: List Volumes
      description: Lists the iSCSI stored volumes of a gateway.
      operationId: listVolumes
      x-api-path-slug: actionlistvolumes-get
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