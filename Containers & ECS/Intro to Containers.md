
#### Personal Summary 

 - Container runs within a clean environment within a Host OS. 
 - Has it's own file system and can run child processes. Can run a web or application server. 
 - Consumers a fraction of memory compared to having multiple apps running on the host Host OS. 
 - Each container runs a separate application. 
 - As an instance is a running copy of it's assigned EBS boot volume; a container is a running copy of a Docker Image. 
 - Dockerfile - used to build Docker images. Each step creates fs layers. 
 - Images are created from a base Image or scratch. 
 - First line of the dockerfile instructs docker to create docker file using a based image.
 - The next line apply software updates and installs the webserver. 
 - Another layer consisting of the script of the dockerfile.  THREE LAYERS TOTAL.
 - A docker container has an additional read & write layer compared to the dockerfile that allows applications to run properly.
 - Docker Containers created from the same dockerimage have differing read & write layers . Shared fs layers = efficient. 

 - Container Registry: container for docker images. These images can be used to create many unique containers within these docker hosts. 
 - Containers are portable, self-contained, and always run as expected. 
 - Lightweight- Parent OS used, fs layers are shared
- Container only runs the application & environment it needs. 
- Ports are 'exposed' to the host and beyond
- Application stacks can be multi-container