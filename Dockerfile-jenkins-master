FROM docker:19.03.12
FROM jenkins/jenkins:2.250-alpine


ENV JENKINS_USER admin
ENV JENKINS_PASS admin

# Skip initial setup
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

# Plugins for better UX (not mandatory)
RUN /usr/local/bin/install-plugins.sh ansicolor
RUN /usr/local/bin/install-plugins.sh greenballs

# Plugin for scaling Jenkins agents
RUN /usr/local/bin/install-plugins.sh kubernetes

# Plugins for Jenkins usage
RUN /usr/local/bin/install-plugins.sh git
RUN /usr/local/bin/install-plugins.sh docker-plugin
RUN /usr/local/bin/install-plugins.sh workflow-aggregator

USER jenkins
