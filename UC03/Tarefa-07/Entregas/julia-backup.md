# Clonagem do Clonezilla 

* **Aluno(a):** Julia Mariany de Lima
* **Tema:** Clonagem de disco para disco 

## 1. Objetivo
O objetivo é clonar um disco para outro com o Clonezilla, copiando sistema, programas e arquivos. Assim dá pra trocar o HD por SSD ou trocar um disco com defeito sem precisar reinstalar tudo.

## 2. Ferramentas e Cuidados Técnicos
* **Ferramentas / Softwares:** Clonezilla Live em imagem ISO.
2 discos conectados: disco antigo (origem) e disco novo (destino).
Cabo SATA e adaptador USB-SATA, se precisar.
Máquina virtual ou computador para dar boot pela imagem ISO.
* **Segurança / Boas Práticas:** Conferir qual disco é a origem e qual é o destino antes de começar, para não apagar o disco errado.
Fazer backup dos arquivos importantes antes da clonagem.
Verificar se o disco novo é igual ou maior que o antigo.
Manter o computador ligado na energia durante todo o processo, sem desligar.
## 3. Passo a Passo
1. Baixar a imagem ISO do Clonezilla Live.
2. Abrir a máquina virtual e anexar a imagem.
3. Adicionar os dois discos na máquina virtual: o disco antigo (origem) e o disco novo (destino).
4. Iniciar a máquina virtual dando boot pela imagem ISO do Clonezilla.
5. Na tela Clonezilla, escolher a opção "device-device" e depois "disk_to_local_disk".
6. Selecionar o disco de origem (antigo) e depois o disco de destino (novo).
7. Conferir a operação e esperar a clonagem terminar,sem desligar.
8. Quando terminar, desligar, tirar a ISO e iniciar só com o disco novo.

## 4. Como Validar (Teste Final)
- O computador ligou normalmente só com os disco novo.
- O sistema abriu com os mesmos programas, arquivos e configurações de antes.
  O disco novo aparece no sistema com o tamanho correto.
