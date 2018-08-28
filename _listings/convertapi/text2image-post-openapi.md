---
swagger: "2.0"
x-collection-name: ConvertAPI
x-complete: 0
info:
  title: Convert API Text to Image
  description: The API for converting Textual files to PDF files and Images. These
    file formats txt, log can be converted to png, jpg, tif.
  version: v1
host: do.convertapi.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /RichText2Image:
    post:
      summary: Rich Text to Image
      description: The API for converting Rich Text documents to PDF files and Images.
        These file formats rtf can be converted to png, jpg, tif.
      operationId: richtext2image
      x-api-path-slug: richtext2image-post
      parameters:
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: File
        description: 'Supported source file formats: rtf'
      - in: query
        name: ImageResolutionH
        description: Image horizontal resolution (DPI)
      - in: query
        name: ImageResolutionV
        description: Image vertical resolution (DPI)
      - in: query
        name: JpgQuality
        description: Jpg image quality
      - in: query
        name: OutputFormat
        description: Supported output file formats png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      responses:
        200:
          description: OK
      tags:
      - Rich
      - Text
      - Image
  /RichText2Pdf:
    post:
      summary: Rich Text to PDF
      description: The API for converting Rich Text documents to PDF files and Images.
        These file formats rtf can be converted to pdf, pdfa, png, jpg, tif.
      operationId: richtext2pdf
      x-api-path-slug: richtext2pdf-post
      parameters:
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: DocumentAuthor
        description: Set the author of the generated Pdf file
      - in: query
        name: DocumentKeywords
        description: Set the keywords of the generated Pdf file
      - in: query
        name: DocumentSubject
        description: Set the subject of the generated Pdf file
      - in: query
        name: DocumentTitle
        description: Set the title of the generated Pdf file
      - in: query
        name: File
        description: 'Supported source file formats: rtf'
      - in: query
        name: OutputFormat
        description: Supported output file formats pdf, pdfa, png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      responses:
        200:
          description: OK
      tags:
      - Rich
      - Text
      - PDF
  /Text2Image:
    post:
      summary: Text to Image
      description: The API for converting Textual files to PDF files and Images. These
        file formats txt, log can be converted to png, jpg, tif.
      operationId: text2image
      x-api-path-slug: text2image-post
      parameters:
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: File
        description: 'Supported source file formats: txt, log'
      - in: query
        name: ImageResolutionH
        description: Image horizontal resolution (DPI)
      - in: query
        name: ImageResolutionV
        description: Image vertical resolution (DPI)
      - in: query
        name: JpgQuality
        description: Jpg image quality
      - in: query
        name: OutputFormat
        description: Supported output file formats png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      responses:
        200:
          description: OK
      tags:
      - Text
      - Image
  /Text2Pdf:
    post:
      summary: Text to PDF
      description: The API for converting Textual files to PDF files and Images. These
        file formats txt, log can be converted to pdf, pdfa, png, jpg, tif.
      operationId: text2pdf
      x-api-path-slug: text2pdf-post
      parameters:
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: DocumentAuthor
        description: Set the author of the generated Pdf file
      - in: query
        name: DocumentKeywords
        description: Set the keywords of the generated Pdf file
      - in: query
        name: DocumentSubject
        description: Set the subject of the generated Pdf file
      - in: query
        name: DocumentTitle
        description: Set the title of the generated Pdf file
      - in: query
        name: File
        description: 'Supported source file formats: txt, log'
      - in: query
        name: OutputFormat
        description: Supported output file formats pdf, pdfa, png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      responses:
        200:
          description: OK
      tags:
      - Text
      - PDF
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