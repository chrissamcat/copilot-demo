FROM 233617426612.dkr.ecr.eu-west-1.amazonaws.com/java-images:maven as maven
COPY . /
WORKDIR /
RUN mvn package

FROM 233617426612.dkr.ecr.eu-west-1.amazonaws.com/java-images:8jre as jre
COPY --from=maven /target/springboot-interceptor-0.0.1.jar /springboot-interceptor-0.0.1.jar
ENTRYPOINT ["java", "-jar", "/springboot-interceptor-0.0.1.jar"]
