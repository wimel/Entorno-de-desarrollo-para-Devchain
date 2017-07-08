# Instalacion en Ubuntu 14.04Lts-64bit del entorno de desarrollo para Devchain sevilla

- Aquí su pagina en Github:
 " https://github.com/DevchainUserGroup/environment "


- Actualizamos primero :

   ~ sudo apt-get update


- Si tenemos otra versión de Ubuntu puede ser que tengamos que instalar vagrant:

   ~ sudo apt-get install vagrant


- Instalamos VirtualBox (maravilloso apt-get):

   ~ sudo apt-get install virtualbox


- Aconsejan instalar el Extension Pack para un mejor funcionamiento, por si acaso lo dejo por aquí también:

   ~ wget -c http://download.virtualbox.org/virtualbox/4.3.10/Oracle_VM_VirtualBox_Extension_Pack-4.3.10-93012.vbox-extpack


- En caso de no tener git instalado lo instalamos:

   ~ sudo apt-get install git


- Clonamos el repositorio:

   ~ git clone https://github.com/DevchainUserGroup/environment.git


- Configuramos el nombre del nodo, uso nano pero podéis usar cualquier otro editor:

   ~ nano ./environment/docker/geth/env.sh


- Entramos en la carpeta Vagrant:

   ~ cd ./environment/vagrant

- Ejecutamos el comando:

   ~ vagrant up**


** En caso de que al ejecutar el comando, nos de el fallo "the box 'ubuntu/xenial64' could not be found", hay que actualizar vagrant a la versión 1.9.6(o al menos yo no he tenido problemas con esta versión), entramos en https://www.vagrantup.com/downloads.html y descargamos la versión Debian 64bit, se nos abrirá el centro de descargas de Ubuntu y descargamos la actualización. 

- Volvemos a ejecutar el comando:

   ~ vagrant up


- Si todo ha ido bien nos saldrá el siguiente mensaje 
" Bringing machine 'devchain-vm' up with 'virtualbox' provider...
==> devchain-vm: Checking if box 'ubuntu/xenial64' is up to date...
==> devchain-vm: Machine already provisioned. Run `vagrant provision` or use the `--provision`
==> devchain-vm: flag to force provisioning. Provisioners marked to run always will still run.
"
- Accedemos a la imagen:
~ vagrant ssh

- Y listo lo ultimo que nos dice es:

   ~ Welcome to Ubuntu 16.04.2 LTS (GNU/Linux 4.4.0-83-generic x86_64)
* Documentation: https://help.ubuntu.com
* Management: https://landscape.canonical.com
* Support: https://ubuntu.com/advantage

Get cloud support with Ubuntu Advantage Cloud Guest:
http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.


Last login: Wed Jul 5 23:16:39 2017 from 10.0.2.2
ubuntu@ubuntu-xenial:~$ 
