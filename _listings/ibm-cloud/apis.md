---
name: IBM Cloud
x-slug: ibm-cloud
description: The IBM Cloud has been built to help you solve problems and advance opportunities
  in a world flush with data. Whether it&rsquo;s data you possess, data outside your
  firewall, or data that&rsquo;s coming, the IBM Cloud helps you protect it, move
  it, integrate it and unlock intelligence from it &mdash; giving you what it takes
  to prevail in a competitive market.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
x-kinRank: "8"
x-alexaRank: "11207"
tags: Volumes
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/apis.md
specificationVersion: "0.14"
apis:
- name: IBM Containers Create a volume in a space
  x-api-slug: ibm-containers
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/create
  tags: Volumes,Create
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumescreate-post-openapi.md
- name: IBM Containers Create a file share in a space
  x-api-slug: ibm-containers
  description: "This endpoint creates a new file share in a space (corresponding IBM
    Containers command: `cf ic volume fs-create FSNAME FSSIZE FSIOPS`). \n\n A file
    share is a persistent NFS-based (Network File System) storage system that hosts
    Docker volumes in a Bluemix space and allows a user to store and access container
    and app-related files. To store files in a file share, you must create a container
    volume and save the data into this volume.\n\n As soon as you create your first
    volume in a space with the `cf ic volume create VOLNAME` command or the `POST
    /volumes/create` API endpoint, a default file share with 20 GB at 4 IOPS (Input
    Output operations Per Second) is created at no cost. \n\nThe organization manager
    can create file shares with specific storage size and IOPS to meet the storage
    needs of the space. File shares can be provisioned in sizes from 20 GB to 12 TB
    and at IOPS per GB of 0.25, 2 or 4. Run `cf ic volume fs-flavor-list` or call
    the `GET /volumes/fs/flavors/json` API endpoint to retrieve a list of available
    file share sizes. The file share size in relation to the number of IOPS impacts
    the speed that data can be read and written from and to the container volume."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/fs/create
  tags: Volumes,Create
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesfscreate-post-openapi.md
- name: IBM Containers List available file share sizes
  x-api-slug: ibm-containers
  description: 'This endpoint returns a list of available file shares in gigabyte
    (corresponding IBM Containers command: `cf ic volume fs-flavor-list`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/fs/flavors/json
  tags: Volumes,Flavors,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesfsflavorsjson-get-openapi.md
- name: IBM Containers List available file shares in a space
  x-api-slug: ibm-containers
  description: 'This endpoint returns a list of all file shares that are availble
    in a space (corresponding IBM Containers command: `cf ic volume fs-list`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/fs/json
  tags: Volumes,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesfsjson-get-openapi.md
- name: IBM Containers Delete a file share
  x-api-slug: ibm-containers
  description: "This endpoint deletes a file share from a space (corresponding IBM
    Containers command: `cf ic volume fs-rm FSNAME`).\n\n Before you can delete a
    file share, all mounted volumes must be deleted first. To delete a volume, run
    `cf ic volume rm VOLNAME` or call the `DELETE /volumes/{name}` API endpoint. \n\n
    **Note:** To delete a file share you must have been granted organization developer
    rights."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/fs/{name}
  tags: Volumes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesfsname-delete-openapi.md
- name: IBM Containers Inspect a file share
  x-api-slug: ibm-containers
  description: 'This endpoint returns detailed information about a file share (corresponding
    IBM Containers command: `cf ic volume fs-inspect FSNAME`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/fs/{name}/json
  tags: Volumes,Name,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesfsnamejson-get-openapi.md
- name: IBM Containers List all volumes for a space
  x-api-slug: ibm-containers
  description: 'This endpoint returns a list of all volumes that are available in
    the given space (corresponding IBM Containers command: `cf ic volume list`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/json
  tags: Volumes,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesjson-get-openapi.md
- name: IBM Containers Delete a volume
  x-api-slug: ibm-containers
  description: 'Delete a volume with a given name from a space (corresponding IBM
    Containers command: `cf ic volume rm VOLNAME`). To delete a volume, all mounted
    containers must be unmounted first. After the volume is deleted, the data that
    are stored in the volume are lost.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/{name}
  tags: Volumes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesname-delete-openapi.md
- name: IBM Containers Share a volume with another space
  x-api-slug: ibm-containers
  description: This endpoint provisions an existing volume that was created in one
    space to another space within the same organization. Single containers and container
    groups in each space can read and write to the shared volume. The volume remains
    owned by the original space it was created in, including management and billing.
    For example, the volume can be deleted from the original space only.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/{name}
  tags: Volumes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesname-post-openapi.md
- name: IBM Containers Retrieve detailed information about a volume.
  x-api-slug: ibm-containers
  description: 'Retrieve a detailed list of information about a volume that is identified
    by the volume name (corresponding IBM Containers command: `cf ic volume inspect
    VOLNAME`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/{name}/json
  tags: Volumes,Name,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/volumesnamejson-get-openapi.md
- name: IBM Containers
  x-api-slug: ibm-containers
  description: The IBM Cloud has been built to help you solve problems and advance
    opportunities in a world flush with data. Whether it&rsquo;s data you possess,
    data outside your firewall, or data that&rsquo;s coming, the IBM Cloud helps you
    protect it, move it, integrate it and unlock intelligence from it &mdash; giving
    you what it takes to prevail in a competitive market.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: Volumes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/volumes/master/_listings/ibm-cloud/openapi.md
x-common:
- type: x-blog
  url: https://www.ibm.com/blogs/bluemix/
- type: x-crunchbase
  url: https://crunchbase.com/organization/product/ibm-bluemix
- type: x-documentation
  url: https://console.bluemix.net/docs/
- type: x-github
  url: https://github.com/IBM-Cloud
- type: x-twitter
  url: https://twitter.com/IBMcloud
- type: x-website
  url: https://www.ibm.com/cloud/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---