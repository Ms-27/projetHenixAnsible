# Objectifs:
Instancier quatre conteneurs avec Ansible:

    - Un contenant la webapp Mantis
    - Deux contenant une BDD postgres (BDD principal et backup)
    - Un reverse proxy

# Au préalable:
Builder l'image docker

    - debian-ansible/Dockerfile


# Les playbooks:
Exécuter les quatre playbooks

    - 01_deploy_nodes.yml (exécuter en root)
    - 02_deploy_DB.yml
    - 03_deploy_mantis.yml
    - 04_deploy_reverse_proxy.yml 


# Gestion du dump de BDD:
Copie l'export de la BDD du conteneur principal vers le backup

    - 10_dump_DB.yml

# Annexes:
Le fichier vars contient les différentes variables:

    - vars.yml