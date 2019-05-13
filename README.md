<h1>Ansible-Drupal</h1>

<h3>Receta Ansible para la instalación de drupal</h3>

Utilización de máquinas virtuales vagrant

Para iniciar los nodos, ejecutamos el siguiente comando dentro del repositorio:

<strong>``vagrant up``</strong>

A continuación comprobamos que tenemos conexión a través de Ansible:

<strong>``ansible all -m ping``</strong>

La respuesta debe ser:

``10.0.0.20 | SUCCESS => {``<br>
``    "changed": false, ``<br>
``    "ping": "pong"``<br>
``}``<br>
``10.0.0.21 | SUCCESS => {``<br>
``    "changed": false, ``<br>
``    "ping": "pong"``<br>
``}``<br>


Para terminar ejecutamos la receta, ejecutando el siguiente parámetro:

<strong>``ansible-playbook site.yml``</strong>

Añadimos el servidor DNS para que pueda resolver el nombre de dominio, la ip del servidor es:

<strong>10.0.0.20</strong>

Accedemos a drupal a través de un navegador web:

<strong>www.drupal8.org</strong>

Usuario: admin
Contraseña: admin
