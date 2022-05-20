# Laboratório: Servidor Web Simples

Para o laboratório, vamos utilizar máquina virtual com Virtualbox. Usaremos o Ubuntu Server 18.04.6 LTS que receberá o NGINX e suas configurações.

Para agilizar a criação da VM, disponibilizo uma imagem .ova já com o Ubuntu instalado. Basta baixar e importar o arquivo no virtualbox.
Ou se preferir criar a VM do zero, o link do para download da imagem do Ubuntu Server 18.04.6 LTS é https://releases.ubuntu.com/18.04/ubuntu-18.04.6-live-server-amd64.iso .

Link Ubuntu 18.04.6 LTS https://releases.ubuntu.com/18.04/ubuntu-18.04.6-live-server-amd64.iso <br/>
Link .OVA https://drive.google.com/file/d/1fPMmhSAx6sHQBIFs9N3CVE0Yaot2XlD4/view?usp=sharing

# Importando arquivo .OVA

Abra o Virtualbox, vá em File > Import Appliance..., ou use o atalho CTRL + I

Em seguida clique no icone folder e selecione o arquivo .ova e clique em OK.
![image](https://user-images.githubusercontent.com/58611969/169564284-0bfdbd3c-1392-4388-a4a9-66cff9704648.png)

Clique em Next>, então clique em Import
![image](https://user-images.githubusercontent.com/58611969/169564700-b5f3fe10-23ba-49ef-8883-98addeca2418.png)

Agora é só aguardar.

# Configurando network interface do Virtualbox

Selecione a VM, clique em Settings (ícone da engrenagem). Na nova janela procure no menu esquero a opção Network. 
Troque a opção NAT para a opção Bridged Adapter.
![image](https://user-images.githubusercontent.com/58611969/169574154-11d56ecb-6508-4442-ada4-d791f17de42a.png)
![image](https://user-images.githubusercontent.com/58611969/169574191-3d550b31-189c-4619-8c79-695983464e54.png)

Com a VM pronta, vamos ligá-la.

user: user
pwd: 12345

# Instalando NGINX

sudo apt update && sudo apt install nginx -y

![image](https://user-images.githubusercontent.com/58611969/169571852-325ef77a-8adc-4793-b56d-8696bb7029ab.png)

# Conferindo se o serviço do NGINX está ativo.

sudo systemctl status nginx.service

![image](https://user-images.githubusercontent.com/58611969/169572440-fad2f2ca-8bbd-4b7d-8d92-e87e535e7599.png)

CTRL + C para encerrar a visualização do serviço.

# Diretórios e arquivos importantes

Diretório de hospedagem da página web
/var/www/html/

Diretório root do NGINX (contém a página Welcome to nginx!)
/usr/share/nginx/html/

Arquivo de configuração
/etc/nginx/nginx.conf




