# Avaliação 01 · Sistema de auditoria de hardware no Excel

[Índice da UC01](../../README.md) · [Atividade no AVA](https://ava.mg.senac.br/edu/mod/assign/view.php?id=608563)

## Orientações da turma

PROJETO FINAL: SISTEMA COMPLETO DE AUDITORIA DE HARDWARE
OBJETIVO: Construir um validador de setup de computadores operando diretamente na nuvem.
O sistema deve importar bases de dados em texto, cruzar especificações físicas e elétricas, e emitir laudos automáticos de gargalo ou incompatibilidade.
Ao final, renomeie o arquivo para AVALIAÇÃO - SEUNOME, baixe uma cópia e entregue nesta tarefa.
1. Preparação do Ambiente e Importação (Excel Online)
Inicie configurando seu banco de dados na nuvem através da importação de arquivos .txt (em anexo).
Acesse o Excel Online pelo seu navegador e abra uma Nova pasta de trabalho em branco.

Aplique o Modo Claro: selecione todas as células, altere a cor de preenchimento para bege e a cor da fonte para laranja ou ciano.

Na barra de menus superior, clique na guia Dados e localize o botão Obter Dados (ou De Texto/CSV).

Selecione o arquivo CPU_Database.txt salvo no seu computador.

Na janela de visualização da importação, certifique-se de que a opção Delimitador esteja configurada como Ponto e vírgula (;) para que o Excel separe as colunas corretamente.

Clique em Carregar.

Repita o processo de importação para os arquivos de RAM_Database.txt, PSU_Database.txt e MOBO_Database.txt.

Observe os dados técnicos importados: a base reflete o mercado real, onde processadores Intel da 12ª Geração utilizam o soquete LGA1700 com suporte a DDR4 e DDR5, enquanto os processadores Ryzen Série 9000 exigem o soquete AM5 e operam nativamente com DDR5.
2. Construção do Painel de Interface
Crie uma nova aba chamada Painel_Auditoria. Esta será a interface ("Front-end") que o cliente utilizará.
Crie quatro campos de entrada de dados para que o usuário escolha o modelo da CPU, Placa-Mãe, RAM e Fonte.

Crie menus suspensos que puxem os modelos diretamente das abas de banco de dados.

Abaixo de cada escolha, crie campos informativos e utilize fórmula para buscar automaticamente as especificações da peça selecionada (Soquete, Tipo DDR, Frequência e Consumo/TDP).
3. Programação do Sistema
Construa o motor lógico do sistema ("Back-end") criando uma seção de diagnóstico no final do painel. Aplique fórmulas para automatizar a auditoria.
Geração de ID: Extraia as 3 primeiras letras do modelo da CPU e junte com a potência da fonte para criar um código de orçamento único.

Auditoria de Soquete: O processador e a memória devem encaixar fisicamente na placa-mãe. Compare o soquete da CPU e da RAM com o da placa-mãe. Se forem iguais, retorne "COMPATÍVEL" (com formatação de uma cor); se diferentes, "ERRO: SOQUETE INCOMPATÍVEL" (com formatação de outra cor).

Auditoria de Gargalo de RAM: Processadores Intel da 12ª Geração suportam memória DDR5 até 4800 MHz nativamente. Se a frequência da memória escolhida for maior que a frequência máxima suportada pela CPU, o sistema fará um "underclock" forçado da peça. Compare as frequências. Se a RAM for mais rápida que a CPU, retorne "ALERTA: GARGALO DE MEMÓRIA"  (com formatação de outra cor).

Auditoria de Segurança Elétrica: A fonte de alimentação entrega energia baseada na sua eficiência, ditada pelo selo 80 Plus.

Calcule a energia real: multiplique a Potência do Rótulo pela Eficiência.

Calcule o consumo do PC: some o TDP da CPU, o Consumo da RAM e adicione 300W de margem de segurança para a placa-mãe.

Compare o consumo com a energia real. Se o consumo for maior, retorne "RISCO DE QUEIMA: SUBALIMENTADO" (com formatação de uma cor). Caso contrário, "ENERGIA ESTÁVEL" (com formatação de outra cor).

## Anexos publicados no AVA

- [CPU_Database.txt](../Materiais/CPU_Database.txt)
- [MOBO_Database.txt](../Materiais/MOBO_Database.txt)
- [PSU_Database.txt](../Materiais/PSU_Database.txt)
- [RAM_Database.txt](../Materiais/RAM_Database.txt)
