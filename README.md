# vagrant-tfg

Repositorio de Vagrant para el proyecto Ansible "[ansible-tfg](https://github.com/bctorreira/ansible-tfg)", trabajo de fin de grado de Brais Cantorna.

## Detalles

El Vagrantfile aquí alojado hace uso de Oracle VirtualBox. Creará un entorno de 13 máquinas, todas con un usuario `user`, contraseña `abc123.` Sus tarjetas de red serán configuradas en **modo puente**.

Las máquinas definidas son las siguientes:

- x2 nodos de balanceo de carga HTTP (`lbl`)
  - IP lbl1: 192.168.1.131
  - IP lbl2: 192.168.1.132
- x3 nodos de aplicación (`app`)
  - IP app1: 192.168.1.141
  - IP app2: 192.168.1.142
  - IP app3: 192.168.1.143
- x1 nodo de trabajo (`wrk`)
  - IP wrk1: 192.168.1.151
- x2 nodos de balanceo de carga SQL (`sbl`)
  - IP sbl1: 192.168.1.161
  - IP sbl2: 192.168.1.162
- x3 nodos de bases de datos para cluster Galera (`dba`)
  - IP dba1: 192.168.1.171
  - IP dba2: 192.168.1.172
  - IP dba3: 192.168.1.173
- x1 nodo de almacenamiento NFS (`sto`)
  - IP sto1: 192.168.1.181
- x1 nodo de caché de sesiones (`dbr`)
  - IP dbr1: 192.168.1.191

## Uso

Teniendo Oracle VirtualBox y Vagrant instalados, clonar este repositorio en el entorno local. Una vez clonado, situarse en el directorio del repositorio y ejecutar `vagrant up`. Con esto, se aprovisionarán las máquinas necesarias para lanzar sobre ellas el proyecto Ansible anteriormente mencionado. Las máquinas contarán con el usuario `user`, contraseña `abc123.` para realizar con el mismo la configuración inicial (playbook `initial-config.yml`).
