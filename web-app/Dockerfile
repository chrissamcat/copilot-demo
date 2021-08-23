FROM 233617426612.dkr.ecr.eu-west-1.amazonaws.com/java-images:maven as maven
COPY . /
WORKDIR /
RUN mvn -ntp package

FROM 233617426612.dkr.ecr.eu-west-1.amazonaws.com/java-images:8jre as jre
COPY --from=maven /target/spring-boot-complete-0.0.1-SNAPSHOT.jar /spring-boot-complete-0.0.1-SNAPSHOT.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/spring-boot-complete-0.0.1-SNAPSHOT.jar"]
