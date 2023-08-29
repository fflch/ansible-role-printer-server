Senha do ambiente de testes: SuperSenh@1

Pacotes com comandos úteis para gerencia de impressoras:

    apt-get install smbclient -t bullseye-backports

Listando impressoras:

    rpcclient -U "" -N -c 'enumprinters' printers.smbdomain.local.br

Trocando o nome de nova_impressora para new_impressora:

    rpcclient -U Administrator%SuperSenh@1 printers.smbdomain.local.br -c 'setprintername nova_impressora new_impressora'
    
Deixando nomes de duas impressoras vazias:

    rpcclient -U Administrator%SuperSenh@1 printers.smbdomain.local.br -c 'setprintername nova_impressora'
    rpcclient -U Administrator%SuperSenh@1 printers.smbdomain.local.br -c 'setprintername nova2_impressora'

Votando os nomes originais:

    rpcclient -U Administrator%SuperSenh@1 printers.smbdomain.local.br -c 'setprintername nova_impressora nova_impressora'
    rpcclient -U Administrator%SuperSenh@1 printers.smbdomain.local.br -c 'setprintername nova2_impressora nova2_impressora'
