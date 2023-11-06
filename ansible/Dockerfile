# Utilisez une image légère basée sur Python (par exemple, python:3-slim)
FROM python:3-slim

# Installez les dépendances nécessaires pour Ansible
RUN apt-get update && \
    apt-get install -y \
    software-properties-common \
    && rm -rf /var/lib/apt/lists/*

# Installez Ansible
RUN pip install ansible

# Copiez le répertoire Ansible du répertoire actuel (qui est ansible/) vers l'image
COPY . /ansible/

# Définissez le répertoire de travail
WORKDIR /ansible

# Exécutez le playbook Ansible par défaut
CMD ["ansible-playbook", "playbook_docker.yml"]