## HW-7 Docker and Python:
- This project generates a QR code PNG file that contains a URL, such as a GitHub homepage "https://github.com/nisha2110", and can be scanned by any camera to open the target website. 

## Setup:
- Goto Docker.com and Install docker: - https://www.docker.com/get-started/
- signup docker account

## Building the Image
- docker build -t hw-7-qrcode .
## Running the Container:
- The output message from our Docker container is letting know that our program has successfully generated a QR code image file
 and saved it in the specified directory within the container.
 - The image was saved in the /app/qr_codes/ directory inside the container.

- docker run hw-7-qrcode
  - INFO - QR code successfully saved to /app/qr_codes/QRCode_20241105180401.png
  
- The -v .:/app option mounts the current directory (.) on our host machine to /app inside the container.  
- --> docker run -v .:/app hw-7-qrcode
-  QR code successfully saved to /app/qr_codes/QRCode_20241105180457.png
1. Add the QR code image that links to my own GitHub homepage.
  - [QR Code Image] -- https://github.com/nisha2110/HW-7-qrcode/blob/master/qrcode-image.png

2. Add an image of viewing the log of successfully creating the QR code below.

  - docker logs my_qrcodes
    - INFO - QR code successfully saved to /app/qr_codes/QRCode_20241105190532.png
     [Log image] --  https://github.com/nisha2110/HW-7-qrcode/blob/master/log-image.png

## Setting the arg for the url from the terminal:
- docker run -p 8080:80 httpd (This command runs a Docker container with the httpd (Apache web server) image.)

- docker run --name some-wordpress --network some-network -d wordpress (Running a WordPress Container on a Custom Network.)

- docker run --name some-wordpress -p 8080:80 -d wordpress (Running a WordPress Container on Port 8080.) 
 - write http://localhost:8080 in your web browser open wordpresslink like (http://localhost:8080/wp-admin/setup-config.php)

## Basic Docker Commands: 
- Shows a list of all running containers.
    - docker ps

- Removing a Container (for example. some-wordpress)
    - docker stop container_name 


- Listing Docker Images
    - docker rm container_name

- Lists all Docker images available on our machine.
    - docker images

- Removing a Docker Image
    - docker rmi image_name 

- Viewing Logs of a Container

    - docker logs container_name
