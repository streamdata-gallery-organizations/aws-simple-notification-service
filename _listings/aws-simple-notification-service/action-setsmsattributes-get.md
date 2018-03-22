---
swagger: "2.0"
info:
  title: AWS Simple Notification Service API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=SetSMSAttributes:
    get:
      summary: ' Set SMS Attributes '
      description: Use this request to set the default settings for sending SMS messages
        and receiving daily SMS usage reports
      operationId: setSMSAttributes
      parameters:
      - in: query
        name: |-
          attributes
                      , attributes.entry.N.key (key), attributesentry.N.value (value)
        description: The default settings for sending SMS messages from your account
        type: string
      responses:
        200:
          description: OK
      tags:
      - sms
definitions: []
x-collection-name: AWS Simple Notification Service
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