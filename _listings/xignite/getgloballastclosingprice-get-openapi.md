---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Global Historical Get Global Last Closing Price
  description: Returns last closing price for a security.
  version: 1.0.0
host: www.xignite.com
basePath: xGlobalHistorical.json/XigniteGlobalHistorical
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetLastSale:
    get:
      summary: Get Last Sale
      description: Returns Last Sale price for a specific bond as reported by the
        price source selected in the input. Request against this operation counts
        as one hit.
      operationId: GetLastSale
      x-api-path-slug: getlastsale-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Last
      - Sale
  /GetLastSales:
    get:
      summary: Get Last Sales
      description: Returns Last Sale price for the list of bonds specified in the
        input, as reported by the price source selected in the input. Each LastSale
        object in the result counts as one hit.
      operationId: GetLastSales
      x-api-path-slug: getlastsales-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Last
      - Sales
  /GetLastIndustryHeadlines:
    get:
      summary: Get Last Industry Headlines
      description: Return the last press releases since a certain time for an industry.
      operationId: postGetlastindustryheadlines
      x-api-path-slug: getlastindustryheadlines-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Last
      - Industry
      - Headlines
  /GetGlobalLastClosingPrice:
    get:
      summary: Get Global Last Closing Price
      description: Returns last closing price for a security.
      operationId: postGetgloballastclosingprice
      x-api-path-slug: getgloballastclosingprice-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Global
      - Last
      - Closing
      - Price
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