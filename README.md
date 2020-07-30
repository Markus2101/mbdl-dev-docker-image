# mbdl-dev-docker-image

This image is used during development of a Modbus application.  
It is based on Debian and contains all necessary components to build the C++ application. Following custom libraries are included:  
- _libmodbus_ (https://github.com/stephane/libmodbus)  
- _BETTER_ENUMS_ (https://aantron.github.io/better-enums/)  
- _nlohmann/json_ (https://nlohmann.github.io/json/)  
- _pymodbus_ (https://pymodbus.readthedocs.io/en/latest/index.html)  
- _spdlog_ (https://github.com/gabime/spdlog)  
- _boost_ (https://www.boost.org/doc/libs/1_72_0/index.html)  

The Docker image uses the _root_ user by default, but adds a user called _docker_. This way, a non-root user is available when opening the docker image, for instance, inside a Visual Studio Code using a _.devcontainer/devcontainer.json_ file:
```json
{
	"name": "Debian C++ Development",
	"image": "markus2101/mbdl-dev:latest",
	"containerUser": "docker"
}
```  

Latest build on DockerHub: https://hub.docker.com/r/markus2101/mbdl-dev
