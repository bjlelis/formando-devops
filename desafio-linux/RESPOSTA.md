#Respostas:

#**0) Ambiente**

Instalação do Vagrant no windows

Cópia do conteúdo com o git clone no cmd

Subir o Vagrant com o comando vagrant up

Instalação automatizada do CentOS com o Vagrant no VirtualBox

Entrar na VM a partir do Windows usando o comando vagrant ssh

IP 192.168.100.75/24

#**1) KERNEL E BOOT LOADER**

Trocar a senha do root e vagrant pelo GRUB:

Acessei o GRUB e troquei o ro por rw

inseri o caminho init=sysroot/bin/sh

ctrl x

chroot /sysroot/

passwd root e inserção da nova senha do root 

passwd vagrant e inserção da nova senha do root 

Criação do arquivo para fazer a alteração no SELinux: touch /.autolabel

exit

reboot

Loguei como root

instalei o nano com: yum install nano

acessei o arquivo /etc/sudoers e inseri o usuário vagrant como SUDO

Agora deve digitar comandos usando sempre o sudo e sua senha para rodar como root: sudo cat /etc/sudoers

#**2) Criação de usuários:**

Para adicionar o user getup com o UID 1111: adduser getup -u 1111

Para adicionar o usuário getup ao grupo bin: gpasswd -a getup bin

Para alterar para 2222 o GID do grupo getup: groupmod -g 2222 getup

Para colocar o user getup como sudo sem pedir senha: alterar o arquivo /etc/sudoers e inserir: getup ALL=NOPASSWD:ALL

#**3) SSH**

ssh vagrant@192.168.100.75 root, vagrant e getup estão acessando

Impedir o acesso via SSH com senha para o usuário vagrant editando o parametro 'PasswordAuthentication no' no arquivo '/etc/ssh/sshd_config'

Criar chave SSH ECDSA: ssh-keygen -t ecdsa

escolhe o local onde salvar: /home/vagrant/.ssh

escolhe uma frase: em branco

Vai gerar um par de chaves ecdsa: pública e privada

#**Rede**

O ping em 8.8.8.8 já estava funcionando

#O restante, por limitações técnicas minhas, não consegui finalizar, me desculpem. Inclusive quebrei minha máquina virtual. Mas vou me evoluir
e aprender mais sobre git, github, vagrant e as demais disciplinas. Obrigado
