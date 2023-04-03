From tomcat:8.0.51-jre8-alpine
ADD http://centos.excellmedia.net/7.9.2009/isos/x86_64/CentOS-7-x86_64-NetInstall-2009.iso


RUN apk update && apk add --no-cache nmap && \
    apk update && \
    apk add --no-cache \
      chromium \
      harfbuzz \
      "freetype>2.8" \
      ttf-freefont \
      nss


 
COPY ./payment-service/target/*.jar payment-service.jar

EXPOSE 8080

CMD ["java","-jar","payment-service.jar"]                              
