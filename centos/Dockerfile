FROM centos 

RUN yum update -y && yum install -y wget

RUN wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo

RUN rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key

RUN yum upgrade -y && yum update -y && yum install curl vim wget epel-release java-11-openjdk-devel -y && yum install jenkins -y

CMD ["java", "-DJENKINS_HOME=/var/lib/jenkins", "-jar", "/usr/lib/jenkins/jenkins.war"]
