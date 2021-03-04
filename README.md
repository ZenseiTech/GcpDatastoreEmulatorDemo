
### Following: Spring Boot application with Cloud Datastore
https://codelabs.developers.google.com/codelabs/cloud-spring-datastore/#0

### Creating Local Datastore emulator
https://cloud.google.com/datastore/docs/tools/datastore-emulator

### Creating the store:
gcloud config set project my-project-zensei

### start the database ...
gcloud beta emulators datastore start --data-dir=. --host-port "127.0.0.1:8001"

### make sure to use the port of the running datastore server ...

### to setup credential run: 
gcloud auth application-default login

export DATASTORE_EMULATOR_HOST=127.0.0.1:8001
export DATASTORE_PROJECT_ID=my-project-zensei

### If running from the IDE make sure to put the environment variable there
DATASTORE_EMULATOR_HOST=127.0.0.1:8001;DATASTORE_PROJECT_ID=my-project-zensei


### Initializing project
curl https://start.spring.io/starter.tgz -d packaging=war -d dependencies=cloud-gcp -d baseDir=datastore-example -d bootVersion=2.4.0 | tar -xzvf -


### To run the project
./mvnw spring-boot:run