# POP-01: Clonagem de Estações em Rede via Clonezilla Lite Server/Client

Aluno(a): Matheus Santana           
Tema: Backup e Restore (Clonezilla Lite Server/Client)

## 1. Objetivo e Escopo
Padronizar o procedimento de implantação em massa de imagens de sistema operacional 
em rede local (LAN) utilizando o **Clonezilla Lite Server/Client**, garantindo agilidade, 
padronização e integridade dos dados.

## 2. Requisitos e Topologia do Ambiente
* **Servidor (Lite Server):** 4gb de Ram, 4 núcleos, 20gb de armazenamento e a iso do clonezilla
* **Clientes (Lite Clients):** 2 máquinas e 20gb de armazenamento cada
* **Infraestrutura de Rede:** Switch dedicado isolado (sem conflito de DHCP externo)
* **Configurações de BIOS/UEFI:** Boot PXE habilitado; Secure Boot habilitado

## 3. Passo a Passo Operacional 
### 3.1. Configuração do Servidor (`lite-server`) 
1. Iniciar o Clonezilla Live e selecionar `Start_Clonezilla` > `lite-server`. 
2. Configurar a interface de rede com IP estático e definir o pool DHCP. 
3. Selecionar `start-new-lite-server` > `device-device`. 
4. Escolher o modo `massive-deployment` e transmissão `multicast`. 
5. Definir o gatilho de início (`clients-to-wait` = [2] clientes). 
### 3.2. Inicialização dos Clientes (`lite-client`) 
1. Inicializar as estações via boot de rede (PXE). 
2. Validar o recebimento de IP pelo servidor DHCP do Clonezila. 
3. Acompanhar a sincronização e conclusão da gravação em disco. 
## 4. Checklist de Homologação e Pós-Clonagem
 - [x] Sistema operacional inicializa sem erros de boot ou partição.
 - [x] Todos os drivers de hardware e placa de rede estão operacionais. 
 - [x] Hostname alterado individualmente em cada estação clonada. 
 - [x] Identificador único do sistema (SID/Machine-ID) verificado. 
 - [x] Licenciamento de software e conformidade com a LGPD validados. 