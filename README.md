# Ansible-Sonar
Ansible playbook to Install SonarQube on RHEL/CentOS/AWS Linux (tested with AWS Linux)

This playbook tunes the OS to run Sonar as a service, installs Java, installs and configures Sonar.  It requires an existing Postgres Database to connect to.

As is, it is setup to run locally but the host file can be modified to run against a remote system.

To use:

ansible-playbook  sonar.yml --extra-vars "psql_sonar_pw=DB_PASSWORD psql_sonar_un=DB_USERNAME psql_sonar_host=DB_HOST"

