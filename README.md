# containerizing-dotnet-core-mvc-app
1. Install Docker Desktop as per the OS from the link
   https://docs.docker.com/get-docker/

2. Once Docker is installed, open the command prompt with "containerizing-dotnet-core-mvc-app" as path

3. Run below command to create docker image

      `docker build -t [repository-name]/[image-name]:[tag-name]`
   
      e.g: Suppose 

            [repository-name] : XYZ

            [image-name]   :  mvc-app

            [tag-name]     :  1.0
        
      then command to create docker image will be 
   
      `docker build -t XYZ/mvc-app:1.0 .`
   
      [Please note dot in the end of the command which denotes the path of Dockerfile in same location]
   
 4. Push the Image to Repository using command
 
      `docker push [repository-name]/[image-name]:[tag-name]`
   
      e.g: for the image created in step 4, command to push the image to the repository would be
   
      `docker push XYZ/mvc-app:1.0`
   
 5. To run the Application inside the container use below command
  
      `docker run -d -p 8080:80 [repository-name]/[image-name]:[tag-name]`
   
      e.g: for the image created in step 4, command to run the container would be
   
      `docker run -d -p 8080:80 XYZ/mvc-app:1.0`
 
 6. Run below command to check the container created
      
      `docker ps`
      
      This should show you the container created with status and other details like image from which this container is created.
     
 7. Now Run the Application using URL
      
      http://localhost:8080

 8. To Stop container run below command
   
      `docker stop [initial 3-4 characters of container unique id]`
      
 10. To remove the container run the below command
   
      `docker rm [initial 3-4 characters of container unique id]`
      
      After this step, command on step 7 would not list this container as this would be deleted.
      
 11. To remove the image run below command
      
      `docker rmi [repository-name]/[image-name]:[tag-name]`
     
     
[NOTE:] Dockerfile in the project is very importatnt as that is used to cerate the image of the application and corresponding dependencies. 
