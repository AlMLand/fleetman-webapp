# podhodjaschaja dlja prilozhenija jdk
FROM ibm-semeru-runtimes:open-8u345-b01-jdk-jammy

LABEL maintainer="Alex Morland"

# zdes neobhodimo predstavit port, tak kak on ne nasleduetska iz parent dockerfile (ego prosto net tam)
EXPOSE 8080

# predostavljaju rabochuju directorije, poetomu mogu pisat nizhe(pravij) ROOT.jar bez /usr/local/bin/
WORKDIR /usr/local/bin/

# dlja dependency -> io.fabric8:docker-maven-plugin, neobhodimo propisat `/maven/` vmesto `/target/...`
# depandecy samo nahodit jar ili war file v target papke
COPY maven/ ROOT.jar

# vipolnjaju komandu, kak esli bi ja startoval etot jar iz commando line
CMD ["java","-Dspring.profiles.active=docker-demo","-jar","ROOT.jar"]
