# 1 - Criação do setup de ambiente:

![1 EC2](https://user-images.githubusercontent.com/90628508/192902512-2fd322fc-cd2b-4e4e-b886-be8b4155f5a7.png)
![1 gateway de internet](https://user-images.githubusercontent.com/90628508/192902513-c063a065-5514-45ec-9d41-36f127f6b2a2.png)
![1 git](https://user-images.githubusercontent.com/90628508/192902518-d20a0b38-14fe-429b-b5f3-7dbfea239784.png)
![1 subnets](https://user-images.githubusercontent.com/90628508/192902521-5dcff895-2ce0-446f-85c2-aa16d09927c9.png)
![1 tabela de rotas](https://user-images.githubusercontent.com/90628508/192902524-755ee936-1bd2-4795-bf22-f4feba156418.png)
![1 vpc](https://user-images.githubusercontent.com/90628508/192902528-faac9d25-0255-4dac-84a3-1fa623da6204.png)

--------------------------------------------------------------------------------

# 2 - Networking

### Liberei a porta 80 com o protocolo HTTP no Security group da EC2

--------------------------------------------------------------------------------

# 3 - EC2 Access

## 3.1 

### Criar novo par de chaves no console, baixar e liberar a porta 22 (SSH) no Security group
### Descobrir a chave pública através do comando: ssh-keygen -y -f /path_to_download_key-pair.pem
### Em seguida se conectar à instância aatravés do console da AWS e adicionar minha chave pública ao arquivo "authorized_keys"
### Se conectar em seguida ao SSH

##3.2

### Alterei o arquivo /var/www/HTML/index.html usando o nano

---------------------------------------------------------------------------------

# 4 - EC2 troubleshooting

### sudo su
### systemctl start httpd

---------------------------------------------------------------------------------

# 5 - Balanceamento

### Em ações de instância selecionar 'imagem e modelo' e depois 'executar mais como esta' para criar uma instância idêntica
