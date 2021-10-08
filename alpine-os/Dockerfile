FROM alpine

RUN apk update

ARG DEBIAN_FRONTEND=noninteractive

RUN apk add curl openjdk11 vim wget jenkins

CMD ["java", "-DJENKINS_HOME=/var/lib/jenkins", "-jar", "/usr/share/webapps/jenkins/jenkins.war"]
