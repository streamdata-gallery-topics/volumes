---
swagger: "2.0"
x-collection-name: IBM Cloud
x-complete: 0
info:
  title: IBM Containers Retrieve detailed information about a volume.
  description: 'Retrieve a detailed list of information about a volume that is identified
    by the volume name (corresponding IBM Containers command: `cf ic volume inspect
    VOLNAME`).'
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
  /volumes/fs/create:
    post:
      summary: Create a file share in a space
      description: "This endpoint creates a new file share in a space (corresponding
        IBM Containers command: `cf ic volume fs-create FSNAME FSSIZE FSIOPS`). \n\n
        A file share is a persistent NFS-based (Network File System) storage system
        that hosts Docker volumes in a Bluemix space and allows a user to store and
        access container and app-related files. To store files in a file share, you
        must create a container volume and save the data into this volume.\n\n As
        soon as you create your first volume in a space with the `cf ic volume create
        VOLNAME` command or the `POST /volumes/create` API endpoint, a default file
        share with 20 GB at 4 IOPS (Input Output operations Per Second) is created
        at no cost. \n\nThe organization manager can create file shares with specific
        storage size and IOPS to meet the storage needs of the space. File shares
        can be provisioned in sizes from 20 GB to 12 TB and at IOPS per GB of 0.25,
        2 or 4. Run `cf ic volume fs-flavor-list` or call the `GET /volumes/fs/flavors/json`
        API endpoint to retrieve a list of available file share sizes. The file share
        size in relation to the number of IOPS impacts the speed that data can be
        read and written from and to the container volume."
      operationId: this-endpoint-creates-a-new-file-share-in-a-space-corresponding-ibm-containers-command-cf-ic-volume-
      x-api-path-slug: volumesfscreate-post
      parameters:
      - in: body
        name: FileshareParam
        description: The input parameter to create a new file share in a space
        schema:
          $ref: '#/definitions/holder'
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
  /volumes/fs/flavors/json:
    get:
      summary: List available file share sizes
      description: 'This endpoint returns a list of available file shares in gigabyte
        (corresponding IBM Containers command: `cf ic volume fs-flavor-list`).'
      operationId: this-endpoint-returns-a-list-of-available-file-shares-in-gigabyte-corresponding-ibm-containers-comma
      x-api-path-slug: volumesfsflavorsjson-get
      parameters:
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
      - Flavors
      - Json
  /volumes/fs/json:
    get:
      summary: List available file shares in a space
      description: 'This endpoint returns a list of all file shares that are availble
        in a space (corresponding IBM Containers command: `cf ic volume fs-list`).'
      operationId: this-endpoint-returns-a-list-of-all-file-shares-that-are-availble-in-a-space-corresponding-ibm-conta
      x-api-path-slug: volumesfsjson-get
      parameters:
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
      - Json
  /volumes/fs/{name}:
    delete:
      summary: Delete a file share
      description: "This endpoint deletes a file share from a space (corresponding
        IBM Containers command: `cf ic volume fs-rm FSNAME`).\n\n Before you can delete
        a file share, all mounted volumes must be deleted first. To delete a volume,
        run `cf ic volume rm VOLNAME` or call the `DELETE /volumes/{name}` API endpoint.
        \n\n **Note:** To delete a file share you must have been granted organization
        developer rights."
      operationId: this-endpoint-deletes-a-file-share-from-a-space-corresponding-ibm-containers-command-cf-ic-volume-fs
      x-api-path-slug: volumesfsname-delete
      parameters:
      - in: path
        name: name
        description: The name of the file share that you want to delete
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
      - Name
  /volumes/fs/{name}/json:
    get:
      summary: Inspect a file share
      description: 'This endpoint returns detailed information about a file share
        (corresponding IBM Containers command: `cf ic volume fs-inspect FSNAME`).'
      operationId: this-endpoint-returns-detailed-information-about-a-file-share-corresponding-ibm-containers-command-c
      x-api-path-slug: volumesfsnamejson-get
      parameters:
      - in: path
        name: name
        description: The name of the file share that you want to inspect
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
      - Name
      - Json
  /volumes/json:
    get:
      summary: List all volumes for a space
      description: 'This endpoint returns a list of all volumes that are available
        in the given space (corresponding IBM Containers command: `cf ic volume list`).'
      operationId: this-endpoint-returns-a-list-of-all-volumes-that-are-available-in-the-given-space-corresponding-ibm-
      x-api-path-slug: volumesjson-get
      parameters:
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
      - Json
  /volumes/{name}:
    delete:
      summary: Delete a volume
      description: 'Delete a volume with a given name from a space (corresponding
        IBM Containers command: `cf ic volume rm VOLNAME`). To delete a volume, all
        mounted containers must be unmounted first. After the volume is deleted, the
        data that are stored in the volume are lost.'
      operationId: delete-a-volume-with-a-given-name-from-a-space-corresponding-ibm-containers-command-cf-ic-volume-rm-
      x-api-path-slug: volumesname-delete
      parameters:
      - in: path
        name: name
        description: The name of the volume that you want to delete
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
      - Name
    post:
      summary: Share a volume with another space
      description: This endpoint provisions an existing volume that was created in
        one space to another space within the same organization. Single containers
        and container groups in each space can read and write to the shared volume.
        The volume remains owned by the original space it was created in, including
        management and billing. For example, the volume can be deleted from the original
        space only.
      operationId: this-endpoint-provisions-an-existing-volume-that-was-created-in-one-space-to-another-space-within-th
      x-api-path-slug: volumesname-post
      parameters:
      - in: path
        name: name
        description: The name of the volume that you want to share with another space
          in your organization
      - in: body
        name: volumeParam
        description: Input parameter that are required to provision an existing volume
          to a new space and to unprovision it from a space
        schema:
          $ref: '#/definitions/holder'
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
      - Name
  /volumes/{name}/json:
    get:
      summary: Retrieve detailed information about a volume.
      description: 'Retrieve a detailed list of information about a volume that is
        identified by the volume name (corresponding IBM Containers command: `cf ic
        volume inspect VOLNAME`).'
      operationId: retrieve-a-detailed-list-of-information-about-a-volume-that-is-identified-by-the-volume-name-corresp
      x-api-path-slug: volumesnamejson-get
      parameters:
      - in: path
        name: name
        description: The name of the volume, for which you want to retrieve detailed
          information
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
      - Name
      - Json
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