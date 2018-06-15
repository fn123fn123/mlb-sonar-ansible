# Ansible-Sonar
Ansible playbook to Install SonarQube on RHEL/CentOS/AWS Linux (tested with AWS Linux)

This playbook tunes the OS to run Sonar as a service, installs Java, installs and configures Sonar.  It requires an existing Postgres Database and an EFS volume to mount to.

As is, it is setup to run locally but the host file can be modified to run against a remote system.

To use:

export AWS_REGION=XXXXX
export EFS_ID=XXXXX
export DB_HOST=XXXXX
export DB_USERNAME=XXXXX
export DB_PASSWORD=XXXXX

ansible-playbook  sonar.yml --extra-vars "psql_sonar_pw=${DB_PASSWORD} psql_sonar_un=${DB_USERNAME} psql_sonar_host=${DB_HOST} efs_id=${EFS_ID} aws_region=${AWS_REGION}"

