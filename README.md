## Professor: Alaelson Jatobá 
## Disciplina: Infraestrutura e Serviço de Redes
## Data: 08/09/2020 
## Turma: 923 
## Grupo: 4

> ### Integrantes
* Nome: Eduardo Lúcio de Queiroz
* Nome: Natan Ryan Mota Ferreira
* Nome: Pedro Daniel da Silva
* Nome: Kawandy 

# Definições de endereços IPs da Rede e Nomes de Hosts:

## Tabela
```
------------------------------------------------------------------------------------------------------------------------------
|  DESCRICAO         |  IP                  |   hostname                |          FQDN                      |     aliase   |
------------------------------------------------------------------------------------------------------------------------------
| 923-grupo4-vm1     | 192.168.23.58        |   srv-vm1-eduardo     | eduardo.grupo4-923.ifalara.net     |       duardo |
| 923-grupo4-vm2     | 192.168.23.59        |   srv-vm2-natan       | natan.grupo4-923.ifalara.net       |       xama   |
| 923-grupo4-vm3     | 192.168.23.60        |   srv-vm3-pedro       | pedro.grupo4-923.ifalara.net       |       mamute |
| 923-grupo4-vm4     | 192.168.23.61        |   srv-vm4-kawandy     | kawandy.grupo4-923.ifalara.net     |       tigre  |
------------------------------------------------------------------------------------------------------------------------------
```

## Executando o comando cat /etc/hosts
![image](https://user-images.githubusercontent.com/83377894/206257381-b8b9c155-0938-41df-94dc-1cc09f248f48.png)


# Configurando os ambientes

## Hardware de cada VM:
> ### vm1: 923-grupo4-vm1:
- Quantidade de Memória: 512MB
- Quantidade de processadores: 1
- Espaço em disco: 10GB

> ### vm1: 923-grupo4-vm2:
- Quantidade de Memória: 
- Quantidade de processadores: 
- Espaço em disco: 

> ### vm1: 923-grupo4-vm3:
- Quantidade de Memória:
- Quantidade de processadores: 
- Espaço em disco: 

> ### vm1: 923-grupo4-vm4:
- Quantidade de Memória: 
- Quantidade de processadores: 
- Espaço em disco: 

### Baixando o arquivo .ova da máquina virtual com o sistema operacional 

```
scp aluno@192.168.101.55:~/Public/iso-images/ubuntu-server-mini.ova
```

### Antes de iniciar a máquina virtual, baixe o Extension Pack
```
sudo apt install virtualbox-ext-pack
```

## Após isso, você poderá iniciar a VM.

# Na VM:

## Fazendo o login
User: administrador <br />
Senha: adminifal

## Definindo o nome da máquina 1
```
sudo hostnamectl set-hostname srv-vm1-eduardo
```

## Configurando endereço de rede na interface ENS192:

### Modificando arquivo /etc/netplan/01-netcgf.yaml

![image](https://user-images.githubusercontent.com/83377894/206250952-4423b888-993a-4469-b356-59fb94230af2.png)

### Após modificar o arquivo, execute os seguinte comando para aplicar as alterações e vê-las:
```
sudo netplan apply
ifconfig -a
```

## Saída do terminal:
![image](https://user-images.githubusercontent.com/83377894/206257735-189ff830-dd05-430b-b6fd-e86e65ed2402.png)

