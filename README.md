<h1>Ansible-Drupal</h1>

<h3>Receta Ansible para la instalación de drupal</h3>

Utilización de máquinas virtuales vagrant

Para iniciar los nodos, ejecutamos el siguiente comando dentro del repositorio:

``vagrant up``

A continuación comprobamos que tenemos conexión a través de Ansible:

``ansible all -m ping``

La respuesta a este comando debe ser:

``10.0.0.20 | SUCCESS => {``
``    "changed": false, ``
``    "ping": "pong"``
``}``
``10.0.0.21 | SUCCESS => {``
``    "changed": false, ``
``    "ping": "pong"``
``}``

Para terminar ejecutamos la receta, ejecutando el siguiente parámetro:

``ansible-playbooks site.yml``
