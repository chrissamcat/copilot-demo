FROM maven as maven
COPY . /
WORKDIR /
RUN mvn package

FROM openjdk:8-jre as jre
COPY --from=maven /target/springboot-interceptor-0.0.1.jar /springboot-interceptor-0.0.1.jar
ENTRYPOINT ["java", "-jar", "/springboot-interceptor-0.0.1.jar"]
