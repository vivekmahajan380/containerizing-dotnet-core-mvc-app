# containerizing-dotnet-core-mvc-app
1. Install Docker Desktop as per the OS from the link
   https://docs.docker.com/get-docker/

2. To install Docker you would need to Regiter @ https://hub.docker.com. 

3. Once Docker is installed, open the command prompt with "containerizing-dotnet-core-mvc-app" as path

4. Run below command to create docker image
   docker build -t [repository-name]/[image-name]:[tag-name]
   
   e.g: Suppose 
         [repository-name] : XYZ
         [image-name]   :  mvc-app
         [tag-name]     :  1.0
        
   then command to create docker image will be 
   docker build -t XYZ/mvc-app:1.0 .      [Please note dot in the end of the command which denotes the path of Dockerfile in same location.] 
