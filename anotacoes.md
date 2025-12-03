🛡️ ANOTAÇÕES TÉCNICAS – HOME LAB DE CYBERSECURITY

Autor: Pedro Tarram
Usuário do Kali: pedrotec
Projeto: Criação de Ambiente de Laboratório para Prática de Segurança da Informação

1. Introdução

Este documento registra, de forma técnica e objetiva, os procedimentos realizados para a construção do meu primeiro laboratório de Segurança da Informação.
O ambiente foi estruturado utilizando o VirtualBox e o sistema operacional Kali Linux, visando permitir práticas seguras relacionadas a análise de redes, varredura de portas, identificação de serviços e desenvolvimento de habilidades fundamentais em Cybersecurity.
A execução ocorreu inteiramente em ambiente isolado, sem risco para o sistema operacional principal.

2. Objetivo Geral

O objetivo deste laboratório é:

Criar um ambiente controlado para estudo e prática de Segurança da Informação;

Simular cenários básicos enfrentados por analistas de segurança;

Praticar o uso de ferramentas essenciais, como Nmap;

Desenvolver autonomia em Linux e compreensão de redes;

Documentar o processo de forma estruturada e profissional.

3. Instalação do VirtualBox
Objetivo

Instalar o hypervisor responsável por gerenciar máquinas virtuais.

Procedimentos

Acessei o endereço oficial: https://www.virtualbox.org/wiki/Downloads

Realizei o download da versão “Windows Hosts”;

Executei o instalador e concluí o processo com as configurações padrão
(Next → Next → Yes → Install → Finish).

Observação

A utilização do VirtualBox permite a criação de ambientes isolados necessários para treinamento prático em segurança, evitando qualquer comprometimento ao sistema real.

4. Download da ISO do Kali Linux
Objetivo

Obter a imagem oficial utilizada para instalação do Kali Linux.

Procedimentos

Acessei: https://www.kali.org/get-kali/

Realizei o download da versão Installer – 64-bit;

Arquivo obtido no formato .iso.

Observação

A imagem foi baixada exclusivamente do site oficial para garantir integridade e autenticidade.

5. Criação da Máquina Virtual
Objetivo

Configurar a máquina virtual onde o Kali Linux seria instalado.

Configurações adotadas

Nome: Kali Linux

Sistema: Linux

Distribuição: Debian (64-bit)

Memória RAM: 4 GB

Disco virtual: 30 GB (dinamicamente alocado)

Tipo de disco: VDI

Justificativa técnica

Como o Kali Linux é baseado no Debian, a seleção da distribuição Debian (64-bit) garante maior compatibilidade com o kernel durante a instalação.

6. Instalação do Kali Linux
Objetivo

Realizar a instalação completa do Kali Linux dentro da máquina virtual criada.

Procedimentos executados

Inicializei a VM selecionando a ISO do Kali.

Escolhi a opção Graphical Install.

Realizei as configurações iniciais:

Idioma: Português (Brasil)

Região: Brasil

Teclado: Português (Brasil)

Configuração de rede:

Hostname: kali

Domínio: deixado em branco

Criação do usuário:

Nome completo: Pedro Tarram

Nome de login: pedrotec

Senha definida durante o processo

Selecionei o fuso horário: São Paulo.

Particionamento do disco:

Método: Guiado – usar o disco inteiro

Layout: uma única partição para todos os arquivos

Confirmei a gravação das alterações

Instalei o GRUB no disco principal (/dev/sda).

Observação

O GRUB é fundamental para o processo de inicialização da máquina virtual, sendo indispensável para o correto funcionamento do sistema.

7. Primeiro Login

Após a conclusão da instalação e reinicialização automática:

Acessei a tela de login;

Informei o usuário pedrotec e a senha configurada;

O ambiente gráfico foi carregado com sucesso.

Observação

O comportamento de não exibir caracteres ao digitar a senha é padrão em sistemas Linux, por motivo de segurança.
