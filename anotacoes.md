🛡️ ANOTAÇÕES TÉCNICAS – HOME LAB DE CYBERSECURITY

Autor: Pedro Tarram
Usuário do Kali: pedrotec
Projeto: Construção de Ambiente de Laboratório para Estudos de Segurança da Informação

1. Introdução

O presente documento tem como objetivo registrar de maneira formal e estruturada a criação do meu primeiro Laboratório de Segurança da Informação, configurado em ambiente virtualizado por meio do VirtualBox.
Este laboratório é destinado à prática de fundamentos de Cybersecurity, testes controlados, varredura de portas, análise de serviços, documentação de procedimentos e desenvolvimento de habilidades técnicas essenciais para atuação na área.

Toda a execução ocorreu em ambiente isolado, garantindo segurança ao sistema operacional principal.

2. Objetivo Geral do Laboratório

O laboratório foi projetado para:

Proporcionar um ambiente controlado para estudos de Segurança da Informação;

Permitir o uso de ferramentas de análise e testes ofensivos/defensivos;

Simular cenários reais de atuação profissional;

Criar o hábito de documentação formal e técnica;

Desenvolver autonomia operacional em Linux e redes.

3. Instalação do VirtualBox
3.1 Objetivo

Instalar o hypervisor responsável pela criação e gerenciamento de máquinas virtuais.

3.2 Procedimentos executados

Acesso ao site oficial: https://www.virtualbox.org/wiki/Downloads

Download da versão Windows Hosts;

Execução do instalador com as etapas padrão do assistente:
Next → Next → Yes → Install → Finish.

3.3 Observação técnica

O VirtualBox oferece isolamento completo entre o sistema real e os ambientes de teste, permitindo experimentação segura de ferramentas de segurança.

4. Download da ISO do Kali Linux
4.1 Objetivo

Obter a imagem oficial do sistema operacional Kali Linux, amplamente utilizado em testes de segurança.

4.2 Procedimentos executados

Acesso ao site oficial: https://www.kali.org/get-kali/

Seleção da opção Installer – 64-bit;

Download da imagem no formato .iso.

4.3 Observação técnica

A utilização da fonte oficial assegura a integridade da imagem, reduzindo riscos de adulteração.

5. Criação da Máquina Virtual do Kali Linux
5.1 Objetivo

Configurar a estrutura virtual necessária para instalação do Kali Linux.

5.2 Configurações definidas

Informações gerais:

Nome da VM: Kali Linux;

Sistema: Linux;

Distribuição: Debian (64-bit).

Hardware Virtual:

Memória RAM: 4 GB;

Disco virtual: 30 GB (dinamicamente alocado);

Tipo de arquivo: VDI.

5.3 Justificativa técnica

A distribuição Debian foi selecionada devido ao fato de o Kali Linux ser baseado nesta mesma arquitetura, garantindo maior compatibilidade durante a instalação.

6. Instalação do Kali Linux
6.1 Objetivo

Instalar o sistema operacional Kali Linux dentro da máquina virtual criada.

6.2 Procedimentos executados

Início da VM com a imagem .iso selecionada;

Opção escolhida: Graphical Install;

Configurações iniciais:

Idioma: Português (Brasil);

País: Brasil;

Layout do teclado: Português (Brasil).

Configuração de rede:

Hostname: kali;

Domínio: deixado em branco.

Criação do usuário:

Nome completo: Pedro Tarram;

Nome de login: pedrotec;

Senha definida durante a instalação.

Seleção do fuso horário: São Paulo.

Particionamento de disco:

Método: Guiado – usar o disco inteiro;

Layout: todos os arquivos em uma única partição;

Confirmação: gravação das alterações no disco.

Instalação do gerenciador de boot (GRUB) no disco /dev/sda.

6.3 Observação técnica

O GRUB é necessário para inicialização do sistema. Sem sua instalação, a máquina virtual não consegue iniciar corretamente.

7. Primeiro Login no Sistema
7.1 Procedimentos executados

Reinicialização automática ao final da instalação;

Acesso à tela de login;

Inserção das credenciais:

Usuário: pedrotec;

Senha configurada previamente.

7.2 Observação técnica

O Linux oculta senhas durante a digitação por motivos de segurança, não exibindo caracteres no terminal ou na interface.
