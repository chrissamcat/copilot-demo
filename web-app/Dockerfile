FROM maven as maven
COPY . /
WORKDIR /
RUN mvn package

FROM openjdk:8-jre as jre
COPY --from=maven /target/spring-boot-complete-0.0.1-SNAPSHOT.jar /spring-boot-complete-0.0.1-SNAPSHOT.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/spring-boot-complete-0.0.1-SNAPSHOT.jar"]
