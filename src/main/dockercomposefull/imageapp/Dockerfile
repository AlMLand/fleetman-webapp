FROM ibm-semeru-runtimes:open-8u345-b01-jdk-jammy

LABEL maintainer="Alex Morland"

WORKDIR /user/local/bin/

COPY fleetman-0.0.1-SNAPSHOT.jar ROOT.jar

EXPOSE 8080

CMD ["java", "-Dspring.profiles.active=docker-demo", "-jar", "ROOT.jar"]