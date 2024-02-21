# State of the Map Madagascar 2024 Website

This repo is the Jekyll configuration, styles and content powering https://openstreetmap-madagascar.github.io/sotm-madagascar/ or https://2024.stateofthemap.org,

Note that the SotM program is managed through our submission system at https://pretalx.com/sotm2024. If you change it on the submission system, it will be updated on the website automatically. Do that rather than making pull requests on the "session" files here.

## Local installation

### Install Jekyll

See https://jekyllrb.com/docs/installation/

### View locally

* `git clone git@github.com:OpenStreetMap-Madagascar/sotm-madagascar.git`
* `cd sotm-madagascar`
* `jekyll serve -wl`
* Point your browser to `http://localhost:4000/`

## Docker

Alternatively you can use Docker to install Jekyll and to serve the site within a container.

### Using docker-compose

* [Install docker-compose](https://docs.docker.com/compose/install/)
* `git clone git@github.com:OpenStreetMap-Madagascar/sotm-madagascar.git`
* `cd sotm-madagascar`
* `docker-compose up --build`
* Point your browser to `http://localhost:4000/`

Alternatively if you are using docker-machine, replace localhost with the IP address from `docker-machine ip`

## Contributing

### Code Style

Please adhere to the code style rules in the supplied `.editorconfig` file. Instructions for [editors/IDEs](https://editorconfig.org/#download).
