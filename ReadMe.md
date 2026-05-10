Trying GitHub Actions  
  
1.docker pull nginx:alpine 
  
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/171f9ac827e05307cff448a5195733b0b5d59867/images/Screenshot%202026-05-08%20221705.png)  

2. docker run -d -p 8080:80 --name my-nginx nginx:alpine
    
![image alt]()  
4. docker ps  
  
5. docker logs my-nginx
  
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/171f9ac827e05307cff448a5195733b0b5d59867/images/Screenshot%202026-05-08%20221901.png)  

7. docker rm -f my-nginx
  
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/171f9ac827e05307cff448a5195733b0b5d59867/images/Screenshot%202026-05-08%20221933.png)  
