🛡️ Anotações do Laboratório – Pedro Tahan

Este documento reúne minhas anotações do processo de criação e configuração do meu primeiro laboratório de Cybersecurity usando Kali Linux em máquina virtual. A ideia é registrar tudo que eu realmente fiz, passo a passo, desde a instalação até os primeiros testes de rede.

O objetivo é construir um ambiente seguro e controlado para treinar conceitos básicos de segurança da informação e ferramentas fundamentais.

1. Instalação do VirtualBox e criação da VM

Comecei instalando o VirtualBox no Windows, que vai ser o hypervisor responsável por rodar as máquinas virtuais. Depois disso:

Baixei a ISO oficial do Kali Linux diretamente do site kali.org

Criei uma nova máquina virtual com as seguintes configurações:

Tipo: Linux

Versão: Debian (64-bit)

Memória RAM: 4 GB

Disco Virtual: 30 GB (dinâmico)

Placa de rede: NAT (padrão do VirtualBox)

Após isso, iniciei a VM e selecionei a ISO para começar a instalação.

2. Instalação do Kali Linux

Durante o instalador, usei o modo Graphical Install e configurei:

Idioma: Português (Brasil)

Região: Brasil

Teclado: ABNT2

Hostname: kali

Domínio: deixei em branco

Usuário padrão: Pedro Tahan

Nome de login: pedrotech

Fuso horário: São Paulo

Particionamento: usar o disco inteiro

Instalação do GRUB no /dev/sda

Depois da instalação, reiniciei e fiz login normalmente com o usuário:

pedrotech

3. Atualização inicial do sistema

Assim que entrei na interface do Kali, abri o terminal para atualizar o sistema inteiro.

Comandos executados:

sudo apt update
sudo apt upgrade -y


Essa etapa é essencial para garantir que todos os pacotes estejam atualizados, além de corrigir possíveis erros da instalação inicial.

4. Identificação do IP da máquina

Para verificar a configuração de rede e descobrir o endereço IP da VM, executei:

ip a


Encontrei o IP da interface NAT, que nesse formato costuma ser algo como:

10.0.2.15


Esse endereço é importante para qualquer teste de rede.
Salvei o print dessa saída como:

prints/ip-a.png

5. Primeiro teste de varredura com o Nmap

Com o IP identificado, fiz meu primeiro teste real no laboratório: um auto-scan da própria máquina usando Nmap.

Comando utilizado:

sudo nmap 10.0.2.15


A saída que recebi foi a seguinte:

Host is up (0.0000050s latency).
All 1000 scanned ports on 10.0.2.15 are in ignored states.
Not shown: 1000 closed tcp ports (reset)
Nmap done: 1 IP address (1 host up) scanned in 0.09 seconds

Interpretação do resultado (minha análise)

O host está ativo → o Kali está se comunicando na rede NAT normalmente.

Todas as portas estavam fechadas → não havia nenhum serviço rodando.

O estado reset indica que a máquina está enxuta e segura.

Nenhuma porta aberta → comportamento normal para uma instalação limpa.

Print salvo como:

prints/nmap-inicial.png

6. Teste básico de conectividade

Para confirmar que estava tudo funcionando, testei ping externo e interno:

ping -c 4 google.com
ping -c 4 10.0.2.15


Os dois retornaram resposta, confirmando:

A máquina acessa a internet

A interface NAT está funcionando

O sistema está respondendo pacotes ICMP normalmente

7. Situação atual do laboratório

Até aqui, eu já tenho:

Uma máquina Kali totalmente instalada e configurada

Sistema atualizado e estável

Rede NAT funcional

Endereço IP verificado

Primeira análise com Nmap concluída

Prints registrados na pasta prints/

Relatório técnico da varredura armazenado em:

relatorios/relatorio-nmap-inicial.md


Essa é a base do meu laboratório, a partir daqui, posso começar a expandir o ambiente com novas etapas.
