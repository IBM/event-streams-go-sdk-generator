# event-streams-go-sdk-generator
Code Generation Project to Create the Golang SDK for the "IBM Cloud Event Streams Administration API"

## Usage
To download (from command-line):
```
go get github.com/IBM/event-streams-go-sdk-generator v1.0.0
```

Then import the generated client:
```
eventstreams "github.com/IBM/event-streams-go-sdk-generator/build/generated"
```
See the generated [documentation](build/generated/READcliME.md) for details about the client.

## Code Generation
###### NOTE: This SDK Generation project/Guide uses the OpenAPI Generator Gradle Plugin (version "4.3.0"). This is used for Open API 3.x specification (swagger) documents. 

### How to generate the Event Streams Administration Golang Client
- Validate the Swagger definition: `./gradlew openApiValidate`
- Generate the Go code via gradle task: `./gradlew openApiGenerate`

### How to update the Swagger definition
- Download the newest Swagger spec from https://github.com/ibm-messaging/event-streams-docs/blob/master/admin-rest-api/admin-rest-api.yaml and save it as `documentation/swagger.yaml`.
- In the file build.gradle, change the value of `majorMinorVersion` to reflect whatever changes were made in the Swagger definition since the last client generation (using semantic versioning).
- When ready to "publish" the new version, simply push the newly generated code changes. Then once it's in main, tag the main branch with "v\<majorMinorVersion\>", which will allow the new version to be accessible by other go code. For example, to publish the 1.0.2 version, you'd run the following git commands:
  - git tag v1.0.2
  - git push origin v1.0.2
  
## Contributions
Follow the instructions above to make changes to the API specification and regenerate the code. Make the changes in a fork and then submit a pull request.
