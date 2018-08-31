---
swagger: "2.0"
x-collection-name: Google Dataflow
x-complete: 0
info:
  title: Google Cloud Dataflow API Update Project Job
  description: Updates the state of an existing Cloud Dataflow job.
  contact:
    name: Google
    url: https://google.com
  version: v1b3
host: dataflow.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1b3/projects/{projectId}/WorkerMessages:
    post:
      summary: Send Worker Message
      description: Send a worker_message to the service.
      operationId: dataflow.projects.workerMessages
      x-api-path-slug: v1b3projectsprojectidworkermessages-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: projectId
        description: The project to send the WorkerMessages to
      responses:
        200:
          description: OK
      tags:
      - Worker Message
  /v1b3/projects/{projectId}/jobs:
    get:
      summary: Get Project Jobs
      description: List the jobs of a project.
      operationId: dataflow.projects.jobs.list
      x-api-path-slug: v1b3projectsprojectidjobs-get
      parameters:
      - in: query
        name: filter
        description: The kind of filter to use
      - in: query
        name: location
        description: The location that contains this job
      - in: query
        name: pageSize
        description: If there are many jobs, limit response to at most this many
      - in: query
        name: pageToken
        description: Set this to the next_page_token field of a previous responseto
          request additional results in a long list
      - in: path
        name: projectId
        description: The project which owns the jobs
      - in: query
        name: view
        description: Level of information requested in response
      responses:
        200:
          description: OK
      tags:
      - Job
    post:
      summary: Create Project Job
      description: Creates a Cloud Dataflow job.
      operationId: dataflow.projects.jobs.create
      x-api-path-slug: v1b3projectsprojectidjobs-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: location
        description: The location that contains this job
      - in: path
        name: projectId
        description: The ID of the Cloud Platform project that the job belongs to
      - in: query
        name: replaceJobId
        description: Deprecated
      - in: query
        name: view
        description: The level of information requested in response
      responses:
        200:
          description: OK
      tags:
      - Job
  /v1b3/projects/{projectId}/jobs/{jobId}:
    get:
      summary: Get Project Job
      description: Gets the state of the specified Cloud Dataflow job.
      operationId: dataflow.projects.jobs.get
      x-api-path-slug: v1b3projectsprojectidjobsjobid-get
      parameters:
      - in: path
        name: jobId
        description: The job ID
      - in: query
        name: location
        description: The location that contains this job
      - in: path
        name: projectId
        description: The ID of the Cloud Platform project that the job belongs to
      - in: query
        name: view
        description: The level of information requested in response
      responses:
        200:
          description: OK
      tags:
      - Job
    put:
      summary: Update Project Job
      description: Updates the state of an existing Cloud Dataflow job.
      operationId: dataflow.projects.jobs.update
      x-api-path-slug: v1b3projectsprojectidjobsjobid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: jobId
        description: The job ID
      - in: query
        name: location
        description: The location that contains this job
      - in: path
        name: projectId
        description: The ID of the Cloud Platform project that the job belongs to
      responses:
        200:
          description: OK
      tags:
      - Job
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