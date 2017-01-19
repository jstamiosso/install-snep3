# install-snep3
<h2>Assistente para primeira instalação do SNEP3 no debian 8 Jessie</h2>

  A proposta deste script é realizar a preparação do S.O. instalando todos os pacotes necessários para a compilação do Asterisk 13 e a instalação dos pacotes pré-requisitos para o funcionamento do SNEP3.
  
  Dentre as rotinas será executado:
  1. Alteração no sources.list, incluíndo os repositórios do Backports, Multimedia, Docker e do SNEP;
  2. Instalação das chaves GPG necessárias para os repositórios acrescidos;
  3. Serão instalados os seguintes pacotes:
    1. Servidor Web Apache2;
    2. Servidor de Banco de Dados Mysql5;
    3. Pacotes dependencias para compilação do Asterisk 13; e
    4. Servidor de Aplicação PHP5.
  4. Download da versão estável do Asterisk 13;
  5. Descompactação e compilação do Asterisk;
  6. Ativação da inicialização automática do Asterisk 13;
  7. Download da versão estável do SNEP3;
  8. Ajustes necessários no SNEP3 (arquivos de som, permissões de arquivos/diretórios e links simbólicos);
  9. Importação da estrutura das tabelas bem como a carga inicial do banco do SNEP3;
    
  Como utilizar este script:
    1. Instale o debian 8 Jessie básico;
    2. Abra um terminal e logue como root;
    3. Baixe o script para a máquina: caso esteja atrás de um proxy informe ao git da seguinte forma (git config --global http.proxy http://usuarioproxy:senhaproxy@ipproxy:porta/)
      git clone https://github.com/jstamiosso/install-snep3.git
    4. Entre no diretório do projeto:
      cd install-snep3
    5. Torne-o script executável:
      chmod +x install-snep3
    4. Execute-o:
      ./install-snep3
    5. Informe se sua rede possui proxy;
    6. Informe a url do proxy no seguinte formato: hrrp://usuarioproxy:senhaproxy@ipproxy:porta/
    7. Se ocorrer algum erro durante a execução o script irá parar e mostrar o erro, ao executá-lo novamente irá iniciar do ponto onde ocorreu o erro em diante;
    8. Aguarde até o final e tudo estará pronto para utilizar; e
    9. Acesse pelo navegador de qualquer máquina da rede e informe o endereço ip da máquina que foi instalado o SNEP3, logue no sistema e começe a utilizar.
    
