2025-07-23 18:47
Tags: 

# Docker

## Definition

- Tool for containerising the development project, providing it what it need to run starting with the OS, the run-time environment, the dependencies and many more, all isolated inside a container that can be run on any machine, regardless of its configuration.

### [[Images]]

- Are blueprints for the containers to be run, when they are built, they will store the data needed to run.
- It has layers 

### [[Containers]]

- Are the instances of the images, they are the running process of these images.

### [[Volumes]]

- Are a mappings from the current machine to the files and folders inside the image, allowing the change of files on the machine to be mirrored inside the created container without needing to rebuild its image.

## Layer Cashing

- Is a property of Docker images that allow it to cache unchanged layers
