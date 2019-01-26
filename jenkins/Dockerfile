FROM jenkins/jenkins:latest

RUN /usr/local/bin/install-plugins.sh \
  configuration-as-code:latest \
  configuration-as-code-support:latest \
  bitbucket-oauth:latest \
  matrix-auth:latest \
  job-dsl:latest \
  authorize-project:latest \
  workflow-aggregator:latest \
  git:latest \
  cloudbees-bitbucket-branch-source:latest \
  blueocean:latest

# Setting up environment variables for Jenkins admin user
ENV JENKINS_USER admin
ENV JENKINS_PASS admin

# Skip the initial setup wizard
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

ENV CASC_JENKINS_CONFIG /var/jenkins_home/casc_configs

COPY casc_configs /var/jenkins_home/casc_configs
