# Ng8App

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.21.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

docker container run --name jenkins-docker --rm --detach `
    --privileged --network jenkins --network-alias docker `
    --env DOCKER_TLS_CERTDIR=/certs `
    --volume jenkins-docker-certs:/certs/client `
    --volume jenkins-data:/var/jenkins_home `
    --volume C:\repos:/home `
    --dns 192.168.1.1 `
    docker:dind

docker container run --name jenkins-blueocean --rm --detach `
    --network jenkins --env DOCKER_HOST=tcp://docker:2376 `
    --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 `
    --volume jenkins-data:/var/jenkins_home `
    --volume jenkins-docker-certs:/certs/client:ro `
    --volume C:\repos:/home `
    --dns 192.168.1.1 `
    --publish 8080:8080 --publish 50000:50000 jenkinsci/blueocean



    
    --volume $Env:HOMEPATH:/home `