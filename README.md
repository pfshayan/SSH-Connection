# SSH-Connection
ssh connection between ubuntu-containers

SSH CONNECTION

On first(main) container(system):

Install ssh

apt-get install  ssh -y


Start ssh service by using following command:


service ssh start


We need to generate a ssh key pair;
To create a new SSH key pair, you can use ssh-keygen without any arguments
Than change directory to .ssh by using following command:

cd .ssh


OR

cd ~/.ssh


Than read id_rsa.pub file by using following command:

cat id_rsa.pub


Copy all the file.

On other containers(systems):

Install ssh

apt-get install nano ssh


Start ssh service by using following command:

service ssh start


We need to generate a ssh key pair:
To create a new SSH key pair, you can use ssh-keygen without any arguments

Than change directory to .ssh by using following command:

cd .ssh


OR

cd ~/.ssh


Now create a file named ‘authorized_keys’ by using following command:

nano authorized_keys


Now paste the key you copied from id_rsa.pub file from the main container(server).

Note:
         We can make connections in any number of containers by just repeating the other(container) step


