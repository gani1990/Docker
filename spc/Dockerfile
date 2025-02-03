FROM eclipse-temurin:17
LABEL project="learning" 
LABEL author="Gangadhar"
ARG USERNAME=gani
ARG SPC_JAR_URL=https://referenceappslt.s3.ap-south-1.amazonaws.com/spring-petclinic-3.3.0-SNAPSHOT.jar
RUN useradd -m -d /apps -s /bin/bash ${USERNAME}
USER ${USERNAME}
ADD --chown=${USERNAME}:${USERNAME} ${SPC_JAR_URL} /apps/spring-petclinic-3.3.0-SNAPSHOT.jar
WORKDIR /apps
EXPOSE 8080
# CMD Executes when the container is started
CMD [ "java", "-jar", "spring-petclinic-3.3.0-SNAPSHOT.jar" ]
