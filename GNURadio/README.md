# **GUIA DE INSTAÇÃO DO GNU RADIO / USRP's**

## GNU Radio 3.9 / USRP - instalação via LINUX


**Objetivo**
Instalar e configurar o GNU Radio 3.9 no Ubuntu 20.04.3 LTS (Focal Fossa) com suporte a USRP e ao driver RTL-SDR usando o gerenciador de pacotes apt-get.

### Instalação do UHD (Para uso da USRP)**

De acordo com o site https://wiki.gnuradio.org/index.php/InstallingGR#From_Source para utilizar a USRP junto com o GNU Radio é necessário instalar software USRP Hardware Driver (UHD).

Abra o terminal do linux, pode ser feito de duas formas: com o atalho **Ctrl+Alt+T** ou pesquisando na Home a palavra terminal:

**Passo 1:** Para dar inicio a instalação utilize o comando a seguir:

```
sudo apt-get update
sudo apt-get -y upgrade
```

Você verá uma saída similar a:

![](/Imagens/GNUradio/Instalacao/instalacao_linux_01.png)

**Passo 2**: Instalação de dependências necessárias:

```
sudo apt install -y vim git wget cmake g++ libboost-all-dev libgmp-dev swig python3-numpy \
python3-mako python3-sphinx python3-lxml doxygen libfftw3-dev \
libsdl1.2-dev libgsl-dev libqwt-qt5-dev libqt5opengl5-dev python3-pyqt5 \
liblog4cpp5-dev libzmq3-dev python3-yaml python3-click python3-click-plugins \
python3-zmq python3-scipy python3-gi python3-gi-cairo gir1.2-gtk-3.0 \
libcodec2-dev libgsm1-dev
#
pip3 install packaging
#
sudo apt install -y pybind11-dev python3-matplotlib libsndfile1-dev \
python3-pip libsoapysdr-dev soapysdr-tools
pip3 install pygccxml
pip3 install pyqtgraph
#
pip3 install ruamel.yaml gevent mprpc pyudev pyroute2
```

Você verá uma saída similar a:

![](/Imagens/GNUradio/Instalacao/instalacao_linux_02.png)

**Passo 3:** Entre em sua área de trabalho :

```
cd ~
```

**Passo 4:** Com o comando mkdir crie uma pasta chamada workarea:

```
mkdir workarea
```

Você verá uma saída similar a:

![](/Imagens/GNUradio/Instalacao/instalacao_linux_03.png)

**Passo 5:** Entre na pasta criada com o comando cd:
```
cd workarea
```

Você verá uma saída similar a:

![](/Imagens/GNUradio/Instalacao/instalacao_linux_04.png)

**Passo 6:** Instale o uhd:

```
sudo apt-get -y install dpdk
sudo apt-get -y install uhd-host
```

**Passo 7:** Você pode testar isso rapidamente, sem nenhum dispositivo USRP conectado, executando no terminal:

```
uhd_find_devices
```

Você verá uma saída similar a:

![](/Imagens/GNUradio/Instalacao/instalacao_linux_05.png)

**OBS:** Se você estiver emulando uma máquina virtual com o sistema operacional Ubuntu, será preciso habilitar uma segunda placa de rede. Com a máquina desligada, você poderá habilitar a segunda placa de rede indo no menu **Configurações** da máquina no VirtualBox/VMware, ir em **Configurações de Rede** e em **Adaptador** selecionar **Modo Bridge**.

**Passo 9:** Configurar a USRP na máquina virtual.

Agora, com a máquina ligada, você precisa definir um IP Fixo na segunda placa de rede indo no menu **Configurações->Rede** do Ubuntu. Você precisa abrir uma tela similar a figura a seguir.

![](/Imagens/GNUradio/Instalacao/instalacao_linux_06.png)

**Passo 10:** Configurar o IP 198.162.10.1 na segunda placa de rede da máquina virtual e a máscara 255.255.255.0.

![](/Imagens/GNUradio/Instalacao/instalacao_linux_07.png)

**Passo 11:** Com o dispositivo USRP conectado, execute no terminal:

```
uhd_usrp_probe
```

Você verá uma saída similar a:

![](/Imagens/GNUradio/Instalacao/instalacao_linux_08.png)

### Instalação do GNU Radio 3.9


**Passo 1:** Em um terminal, digite os comandos na sequência:

```
sudo add-apt-repository ppa:gnuradio/gnuradio-releases-3.9
sudo apt-get update
sudo apt-get install -y gnuradio
```

**Passo 2:** Vamos baixar o código fonte do GNU RADIO (com alguns exemplos). Em um terminal, digite os comandos na sequência:

```
cd ~/workarea/gnuradio
git clone --recursive https://github.com/gnuradio/gnuradio
git checkout maint-3.9
```

**Passo 3:** O GNURadio pode ser aberto pelo terminal com o comando:

```
gnuradio-companion
```

Ou também pode ser aberto pela sua área de trabalho:

![](/Imagens/GNUradio/Instalacao/instalacao_linux_09.png)

## GNU Radio 3.9 / USRP - instalação via WINDOWS


### Instalação do GNU Radio

Com base no site oficial do GNUradio, é possível utilizar o GNU Radio no Windows. Entretanto, vale salientar que o suporte ao GNU Radio no Windows permanece menos testado e há problemas desconhecidos e até mesmo bugs significativos que afetam o uso regular do GNU Radio Companion.

**Passo 1** - Acesse o site oficial de instalações do GNU Radio, disponível clicando [aqui](https://wiki.gnuradio.org/index.php/InstallingGR). Você verá uma imagem semelhante a:

![](/Imagens/GNUradio/Instalacao/instalacao_windows_01.png)

(Em Manutenção)