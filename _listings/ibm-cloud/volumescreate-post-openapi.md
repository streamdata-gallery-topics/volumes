---
swagger: "2.0"
x-collection-name: IBM Cloud
x-complete: 0
info:
  title: IBM Containers Create a volume in a space
  description: "This endpoints creates a new volume in your space (corresponding IBM
    Containers command: `cf ic volume create VOLNAME`). A volume is used to persist
    and access app data between container restarts. Volumes are hosted on file shares
    that define the available actual storage in Bluemix and the number of input and
    output transactions per second (IOPS). \n\n After you have created a volume, you
    must mount it to a container by using the `--volume` option in the `cf ic run`
    (single containers) or `cf ic group create` (container groups) command. You can
    also define the volume as part of the HTTP body and send a request to the `POST
    /containers/create` (single containers) or `POST /containers/groups` (container
    groups) endpoints. \n\n Note: If you mount multiple containers in a space to the
    same volume, they share the data in the volume and can access them anytime. When
    a container is deleted, the associated volume is not removed."
  version: 3.0.0
host: containers-api.ng.bluemix.net
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /volumes/create:
    post:
      summary: Create a volume in a space
      description: "This endpoints creates a new volume in your space (corresponding
        IBM Containers command: `cf ic volume create VOLNAME`). A volume is used to
        persist and access app data between container restarts. Volumes are hosted
        on file shares that define the available actual storage in Bluemix and the
        number of input and output transactions per second (IOPS). \n\n After you
        have created a volume, you must mount it to a container by using the `--volume`
        option in the `cf ic run` (single containers) or `cf ic group create` (container
        groups) command. You can also define the volume as part of the HTTP body and
        send a request to the `POST /containers/create` (single containers) or `POST
        /containers/groups` (container groups) endpoints. \n\n Note: If you mount
        multiple containers in a space to the same volume, they share the data in
        the volume and can access them anytime. When a container is deleted, the associated
        volume is not removed."
      operationId: this-endpoints-creates-a-new-volume-in-your-space-corresponding-ibm-containers-command-cf-ic-volume-
      x-api-path-slug: volumescreate-post
      parameters:
      - in: query
        name: fsName
        description: The name of the file share that the volume is hosted on
      - in: query
        name: name
        description: The name of the volume
      - in: header
        name: X-Auth-Project-Id
        description: The unique ID of your organization space where you want to create
          or work with your containers
      - in: header
        name: X-Auth-Token
        description: The Bluemix JSON web token that you receive when logging into
          Bluemix
      responses:
        200:
          description: OK
      tags:
      - Volumes
      - Create
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