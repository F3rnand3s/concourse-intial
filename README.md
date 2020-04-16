# concourse-intial
1st Test drive with Concourse CI

docker-compose.yml
 * Docker image of Concourse

running docker-compose:
 1st - cd C:/[directoryOfDockerComposeFile]
 2nd - docker-compose up -d

taking down docker-compose:
 - docker-compose down

fly usefull comands:
 // Autenticate 
 - fly --target testing login --concourse-url http://127.0.0.1:8080 -u USER -p PASSWORD
 - fly --target tutorial sync
 
 // execute task
 - cd [task-dir]
 - fly -t testing execute -c task_hello_world.yml

 // set pipeline
 - fly -t testing set-pipeline -c pipeline.yml -p hello-world