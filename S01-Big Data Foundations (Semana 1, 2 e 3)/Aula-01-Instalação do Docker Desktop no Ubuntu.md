
https://docs.docker.com/desktop/linux/install/ubuntu/

https://docs.docker.com/get-docker/

Instale o Docker Desktop no Ubuntu
Tempo estimado de leitura: 4 minutos

Esta página contém informações sobre como instalar, iniciar e atualizar o Docker Desktop em uma distribuição do Ubuntu.

Pré-requisitos
Para instalar o Docker Desktop com sucesso, você deve:

Atenda aos requisitos do sistema
Tenha uma versão de 64 bits do Ubuntu Jammy Jellyfish 22.04 (LTS) ou do Ubuntu Impish Indri 21.10. O Docker Desktop é suportado na arquitetura (ou ) .x86_64amd64
Desinstale a visualização tecnológica ou a versão beta do Docker Desktop para Linux. Correr:
 sudo apt remove docker-desktop
Para uma limpeza completa, remova a configuração e os arquivos de dados em , o symlink at , e purgue os arquivos de serviço sistematos restantes.$HOME/.docker/desktop/usr/local/bin/com.docker.cli

 rm -r $HOME/.docker/desktop
 sudo rm /usr/local/bin/com.docker.cli
 sudo apt purge docker-desktop
Nota

Se você instalou o Docker Desktop para visualização tecnológica linux ou versão beta, você precisa remover todos os arquivos que foram gerados por esses pacotes (por exemplo, , .~/.config/systemd/user/docker-desktop.service~/.local/share/systemd/user/docker-desktop.service

Além disso, para ambientes desktop não-gnomo, deve ser instalado:gnome-terminal

 sudo apt install gnome-terminal
Instale o Docker Desktop
Abordagem recomendada para instalar o Docker Desktop no Ubuntu:

Configure o repositório do pacote do Docker.

Baixe o último pacote DEB da página de lançamento.

Instale o pacote com o apt da seguinte forma:

 sudo apt-get update
 sudo apt-get install ./docker-desktop-<version>-<arch>.deb
Nota

No final do processo de instalação, exibe um erro devido à instalação de um pacote baixado. Você pode ignorar esta mensagem de erro.apt

 N: Download is performed unsandboxed as root, as file '/home/user/Downloads/docker-desktop.deb' couldn't be accessed by user '_apt'. - pkgAcquire::Run (13: Permission denied)
Existem algumas etapas de configuração pós-instalação feitas através do script pós-instalação contido no pacote deb.

O script pós-instalação:

Define o recurso no binário Docker Desktop para mapear portas privilegiadas e definir limites de recursos.
Adiciona um nome DNS para Kubernetes para ./etc/hosts
Cria um link de ./usr/bin/docker/usr/local/bin/com.docker.cli
Iniciar o Docker Desktop
Para iniciar o Docker Desktop para Linux, pesquise o Docker Desktop no menu Aplicativos e abra-o. Isso lança o ícone do menu de baleias e abre o Painel do Docker, relatando o status do Docker Desktop.

Alternativamente, abra um terminal e execute:

 systemctl --user start docker-desktop
Quando o Docker Desktop é iniciado, ele cria um contexto dedicado que o Docker CLI pode usar como um alvo e define-o como o contexto atual em uso. Isso é para evitar um confronto com um Docker Engine local que pode estar sendo executado no host Linux e usando o contexto padrão. No desligamento, o Docker Desktop redefine o contexto atual para o anterior.

O instalador do Docker Desktop atualiza o Docker Compose e os binários Docker CLI no host. Ele instala o Docker Compose V2 e dá aos usuários a opção de vinculá-lo como docker-compor a partir do painel Configurações. O Docker Desktop instala o novo binário Docker CLI que inclui recursos de integração de nuvem e cria um symlink para o clássico Docker CLI em ./usr/local/bin/usr/local/bin/com.docker.cli

Depois de instalar com sucesso o Docker Desktop, você pode verificar as versões desses binários executando os seguintes comandos:

 docker compose version
 docker --version
 docker version