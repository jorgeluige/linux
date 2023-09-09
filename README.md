# linux

- .vimrc

set mouse-=a
set nocompatible
set nu
syntax on
set encoding=utf-8
set showcmd
filetype plugin indent on

set tabstop=2 shiftwidth=2
set expandtab
set backspace=indent,eol,start

set hlsearch
set incsearch
set ignorecase
set smartcase

color murphy


- .bashrc
PS1='\[\e[1;36m\]\342\224\214\342\224\200\[\e[1;36m\][\[\e[1;36m\]\u\[\e[1;33m\]@\[\e[1;37m\]\h\[\e[1;36m\]]\[\e[1;36m\]\342\224\200\[\e[1;36m\][\[\e[1;37m\]\w\[\e[1;36m\]]\[\e[1;36m\]\342\224\200[\[\e[1;37m\]\t\[\e[1;36m\]]\n\[\e[1;36m\]\342\224\224\342\224\200\342\224\200\342\225\274\[\e[1;32m\] \$ \[\e[0m\]'




# Atualização do Linux. 

Subir pra root
sudo su -

Atualiza os respos:
apt update

verifica se tem pacotes para atualizar
apt install

Atualiza os pacotes. 
apt upgrade -y 

Verificar os arquivos do /boot
ls -lha /boot

Verificar o tamanho de cada arquivo e o somatorio de todos os arquivos.
du -shc /boot/*

Dá um reboot para carregar o novo kernel
reboot 

Verificar a versao do kernel
uname -r

Se quiser verificar todas as informacoes
uname -a

Verificar quais kernels tem instalados
dpkg --list |grep linux-image

removendo o kernel antigo
apt remove linux-image-5.10.0-12-amd64     //aqui e um boa deixar os dois ultimos, o que ta carregando e o anterior, o resto mata. 

dando um puge no kenel antigo, pois mesmo dando remove ainda ficam arquivos de configuracao
apt purge linux-image-5.10.0-12-amd64

limpando temporarios/cache e etc
apt autoclean 
apt autopurge
apt autoremove
apt clean
