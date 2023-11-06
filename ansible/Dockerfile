FROM ubuntu:latest

# Install Ansible and other dependencies
RUN apt-get update && apt-get install -y ansible

# Add your Ansible playbooks and other necessary files
COPY . /ansible

WORKDIR /ansible

CMD [ "ansible-playbook", "playbook_docker.yml" ]
