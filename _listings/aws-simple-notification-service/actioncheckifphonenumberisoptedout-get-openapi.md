---
swagger: "2.0"
x-collection-name: AWS Simple Notification Service
x-complete: 0
info:
  title: AWS Simple Notification Service API Check If Phone Number Is Opted Out
  version: 1.0.0
  description: Accepts a phone number and indicates whether the phone holder has opted
    out of receiving SMS messages from your account.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddPermission:
    get:
      summary: Add Permission
      description: Adds a statement to a topic's access control policy, granting access
        for the specified AWS accounts to the specified actions.
      operationId: addPermission
      x-api-path-slug: actionaddpermission-get
      parameters:
      - in: query
        name: ActionName.member.N
        description: The action you want to allow for the specified principal(s)
        type: string
      - in: query
        name: AWSAccountId.member.N
        description: The AWS account IDs of the users (principals) who will be given
          access to the specified actions
        type: string
      - in: query
        name: Label
        description: A unique identifier for the new policy statement
        type: string
      - in: query
        name: TopicArn
        description: The ARN of the topic whose access control policy you wish to
          modify
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=CheckIfPhoneNumberIsOptedOut:
    get:
      summary: Check If Phone Number Is Opted Out
      description: Accepts a phone number and indicates whether the phone holder has
        opted out of receiving SMS messages from your account.
      operationId: checkIfPhoneNumberIsOptedOut
      x-api-path-slug: actioncheckifphonenumberisoptedout-get
      parameters:
      - in: query
        name: phoneNumber
        description: The phone number for which you want to check the opt out status
        type: string
      responses:
        200:
          description: OK
      tags:
      - Opt Out
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