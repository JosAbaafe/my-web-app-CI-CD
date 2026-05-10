Trying GitHub Actions  
  
1.docker pull nginx:alpine 
  
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/171f9ac827e05307cff448a5195733b0b5d59867/images/Screenshot%202026-05-08%20221705.png)  

2. docker run -d -p 8080:80 --name my-nginx nginx:alpine
    
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/a4d4b9a4f565ac48d839660b8f9c5733a7765abb/images/11.png)  
  
4. docker ps  

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/53e33cf802c300566672b171012d25470e6717bd/images/12.png)  
  
5. docker logs my-nginx
  
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/171f9ac827e05307cff448a5195733b0b5d59867/images/Screenshot%202026-05-08%20221901.png)  

7. docker rm -f my-nginx
  
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/171f9ac827e05307cff448a5195733b0b5d59867/images/Screenshot%202026-05-08%20221933.png)  

8. Open your browser to http://localhost:8080 – you should see the Nginx welcome page.

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/a5caa90e57223df82c6a5c0448e2cef79734fdc4/images/Screenshot%202026-05-08%20221739.png)  

**Phase 1 – Build, Push, Pull & Share Your Own Image**

**Building & Testing Locally**
1. *docker build -t my-web-app .*
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/a5caa90e57223df82c6a5c0448e2cef79734fdc4/images/Screenshot%202026-05-08%20223149.png)

2. *docker run -d -p 5000:5000 --name webapp-test my-web-app *

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/b40206cb8c43a97901d6833279a947d2d217373c/images/2.png)  

3. *Visit http://localhost:5000 and http://localhost:5000/health in your browser.*

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/3.png)  

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/4.png)

**Stop and remove the container when finished**  
  
4. *docker rm -f webapp-test*  

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/5.png)  

5. * docker login -u your-dockerhub-username *

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/6.png)  

6. *docker tag my-web-app your-dockerhub-username/my-web-app:v1.0.0-john*

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/a538e9e48de7056a2932e0c7c672dc0a05ad54af/images/Screenshot%202026-05-08%20231539.png)  

7. *Remove the local image (if it exists – ignore errors).*

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/a538e9e48de7056a2932e0c7c672dc0a05ad54af/images/Screenshot%202026-05-08%20231719.png)  

8. *Pull the image – downloads all layers from the registry.*

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/a538e9e48de7056a2932e0c7c672dc0a05ad54af/images/Screenshot%202026-05-08%20231808.png)  

9. * Run a container from the freshly pulled image, mapping port 5000.*

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/a538e9e48de7056a2932e0c7c672dc0a05ad54af/images/Screenshot%202026-05-08%20231909.png)  

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/f354a97967c2d3b93e56b4a116c21cbf39eeb7f4/images/Screenshot%202026-05-09%20220913.png)  

**Phase 2 – Automate with a DevSecOps Pipeline (GitHub Actions)**  

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/7.png)  

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/8.png)    
  
![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/9.png)  

**Clean Up**  
  
10. *Remove all images and containers created during the lab:*  

![image alt](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/200b700c8251d7a3fde337540210bc117a6dbbc1/images/10.pngg)
  
