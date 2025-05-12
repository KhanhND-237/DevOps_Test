# DevOps_Test
This is DevOps Take-Home Test 

Pre-prerequisite
Installation

1.Docker (ref - https://docs.docker.com/engine/install)
2.Docker Compose v2 ( ref - https://docs.docker.com/compose/install/)
3.Tilt (ref - https://docs.tilt.dev/install.html)
4.NodeJS (ref-https://nodejs.org/en/download)
5.Angular (ref- https://angular.dev/installation)
.....

******************
Step 1 : 
    - Create Go backend server handle route /hello  return "Hello, World!" - in main.go 
    - Create dockerimage for backend - to run container -> Expose port 8080 of container
Step 2 : 
    - Create new agular project with default configuration (run : ng new frontend --defaults)
    - Modify the app.component.html to the content we want ("Welcome to the Frontend")
    - Create dockerimage to frontend and copy artifact we got after build Agular to nginx's directory to render
Step 3 :
    - Create nginx.conf file
    - Overwrite by copy that to configuration file of nginx in dockerfile
Step 4 :
    - Write the docker compose for all services, port mapping,...
Step 5 : 
    - Write Tiltfile to run docker compose file above
Step 6 : 
    - Testing in local with command : tilt up