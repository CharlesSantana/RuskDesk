# RuskDesk

Este programa código aberto ajuda os usuários a acessar e controlar seus computadores de qualquer local. Ele serve como cliente e servidor, portanto, não há necessidade de usar outros aplicativos de terceiros para usá-lo.


## Instalação de Servidor RuskDesk

**Passo a passo**
 
Instalaremos o Servidor RuskDesk

**Necessario para a instalação**

**1- Crie um servidor com uma distro UBUNTU SERVER 22.04 ( foi a minha predileção pelo fato de LTS ) e instale com SSH**

**2- Atualize**

**3- Execute os conteudo abaixo para baixar as suas versões do RuskDesk**

  wget https://github.com/rustdesk/rustdesk-server/releases/download/1.1.7/rustdesk-server-hbbr_1.1.7_amd64.deb
  
  wget https://github.com/rustdesk/rustdesk-server/releases/download/1.1.7/rustdesk-server-hbbs_1.1.7_amd64.deb
  
**4- Instale pelo terminal:**

  sudo dpkg -i rustdesk-server-hbbr_1.1.7_amd64.deb
  
  sudo dpkg -i rustdesk-server-hbbs_1.1.7_amd64.deb
  
**5- Por segurança habilite a regra de entrada do seu firewall para o SSH, somente para o ip de uma maquina local que ira administrá-lo.**

  sudo ufw allow proto tcp from 192.168.0.71 to any port 22
  
**6- Habilite as portas de comunicação da aplicação no Firewall**

  sudo ufw allow 21115:21119/tcp
  
  sudo ufw allow 8000/tcp
  
  sudo ufw allow 21116/udp
  
  sudo ufw enable

**7- Por ultimo ainda no terminal, Execute**

  sudo hbbs -r 192.168.0.73:21115
  
**Obs: este comando ira fazer com que o serviço fique rodando e escutando as conexões**

**Seja Feliz, Seja Livre e Use Linux**
