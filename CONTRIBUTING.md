# Contributing to Enum-Converter

## Developer Certificate of Origin (DCO)

Please sign off your Git commits (```git commit -s```) to indicate that you agree to the terms of [Developer Certificate of Origin](https://developercertificate.org/).

## Recommended knowledge

* Node.js
* Typescript
* Working with Dockers
* Jest

## Development Setup

### Docker Setup

1.  Install Docker Toolbox / Docker
2.  Inside docker cli

    1.  `docker-compose up` - builds the image for live mode
    2.  `docker exec -it enumc bash` - attach to docker shell
    3.  commands
        1.  `cli` - run cli commands
        2.  `debug` - attach debugger to cli commands
        3.  `test` : run jest tests
        4.  `test:watch` : run tests in continues mode
            (not auto updates at the moment because of jest watcher)

### VSCode Docker Debugger Setup

#### launch.json

```
    {
      "type": "node",
      "request": "attach",
      "name": "Attach to Docker",
      "address": "DOCKER_DAEMON_IP",
      "port": 9229,
      "localRoot": "${workspaceFolder}",
      "remoteRoot": "/work"
    },
```

(Note : you might need to add `"outFiles": ["${workspaceFolder}/lib/**/*.js"]` )
