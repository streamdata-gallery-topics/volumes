---
swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 1
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
---