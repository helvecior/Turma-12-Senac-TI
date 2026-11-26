# Prompt para organização de repositório no GitHub para curso técnico em informática

Estou criando um repositorio no git hub para a turma que estuda tecnico em informatica no senac.

## O curso é dividido em 16 unidades curriculares:

- UC1  Planejar e executar a montagem de computadores  Parabéns pelo empenho e compromisso! Mantenha o engajamento e a dedicação.
- UC2  Planejar e executar a instalação de hardware e software para computadores
- UC3  Planejar e executar a manutenção de computadores
- UC4  Projeto Integrador Assistente de Suporte em Manutenção de Computadores
- UC5  Planejar e executar a instalação de redes locais de computadores
- UC6  Planejar e executar a manutenção de redes locais de computadores
- UC7  Planejar e executar a instalação, a configuração e o monitoramento de sistemas operacionais de redes locais (servidores).
- UC8  Projeto Integrador Assistente de Operação de Redes de Computadores
- UC9  Desenvolver algoritmos
- UC10  Desenvolver banco de dados
- UC11  Executar os processos de codificação, manutenção e documentação de aplicativos computacionais para desktop
- UC12  Executar os processos de codificação, manutenção e documentação de aplicativos computacionais para internet
- UC13  Executar os processos de codificação, manutenção e documentação de aplicativos computacionais para mobile
- UC14  Elaborar design de interação para aplicações web
- UC15  Desenvolver e organizar elementos estruturais de sites
- UC16  Projeto Integrador Assistente de Desenvolvimento de Aplicativos Computacionais

> A ideia é manter os materiais acessíveis em um só lugar e facilitar a consulta ao longo do curso.

## Para isso tenho duas opções de organização do repositório, que são

- Criar uma branch para cada unidade curricular, onde cada branch terá os materiais da respectiva unidade.
- Criar apenas uma branch principal (main) e dentro dela criar pastas para cada unidade curricular, onde cada pasta terá os materiais da respectiva unidade.

Quais são as vantagens e desvantagens de cada uma das opções?

## Resposta da IA:

**Para o repositório da turma, eu recomendo manter as 16 unidades em pastas na `main`.** Quem estiver na UC6 e precisar rever um procedimento da UC5 poderá consultar as duas unidades pelo mesmo índice. Isso atende ao seu objetivo de manter o material acessível durante todo o curso.

| Critério | Uma branch por UC | Uma pasta por UC na `main` |
| --- | --- | --- |
| **Consulta pelo GitHub** | O aluno seleciona a branch da disciplina. Isso deixa a tela focada naquela UC, mas exige que a turma saiba usar o seletor de branches. | O aluno abre o repositório e escolhe a pasta da disciplina. Um índice no `README.md` pode mostrar o nome completo de cada UC. |
| **Uso no computador** | Ao trocar de branch, os arquivos da pasta de trabalho passam a refletir a unidade selecionada. Consultar duas UCs lado a lado exige etapas extras. | Um clone reúne as 16 pastas. O aluno pode abrir materiais de várias unidades ao mesmo tempo no VS Code. |
| **Materiais compartilhados** | Um modelo de relatório usado em várias branches precisa ser mantido em cada cópia ou acessado por um link para uma versão central. | Uma pasta `modelos/` pode atender a todas as UCs. Uma correção no modelo fica disponível para a turma em um único lugar. |
| **Histórico de alterações** | Cada UC pode evoluir de forma independente. Isso ajuda quando as branches representam versões diferentes de um mesmo projeto. | O histórico geral reúne as disciplinas, mas dá para consultar só uma delas com `git log -- UC03/`. |
| **Download pelo GitHub** | O ZIP da branch selecionada pode conter apenas os materiais daquela UC, se ela tiver sido organizada assim. | O ZIP da `main` inclui todas as unidades. É prático para baixar o curso inteiro, mas pode ficar grande se houver muitos PDFs e imagens. |

**Como eu organizaria no seu caso:** usaria pastas de `UC01` a `UC16`, com dois dígitos desde a primeira. Assim, **na ordenação por nome**, a `UC02` vem antes da `UC10`, e a sequência independe da ordem de criação. No `README.md` principal, cada linha do índice teria um link como `[UC03 — Planejar e executar a manutenção de computadores](./UC03/)`. A turma poderia localizar a disciplina tanto pelo número quanto pelo assunto.

As branches continuariam úteis para **trabalhos em andamento**. Por exemplo, se um colega quiser atualizar o POP de clonagem da UC3, ele pode criar a branch `revisar-pop-uc03`, editar o documento e abrir um *pull request*. Depois da revisão, a alteração entra na `main`, e a turma encontra a versão atualizada na mesma pasta `UC03/`.

## Prompt após a resposta da IA

Montar um pasta que contenha um README.md que explique:

- o intuito do repo
- como está organizado o repositorio
- tabela que redirecione para as pastas de cada UC mostrando o titulo da UC
- um guia com os comandos mais comuns de operação do repositorio, como por exemplo: branch, pull request, clone, push, sync.  coloque outros que você julgar que vão ajudar.

Como cada UC terá várias tarefas, e como parte delas não tem ainda, faremos uma pasta modelo (chamada Tarefa), que conterá os seguintes componentes:

- Atividades
- Envios
- Materiais

Se você conseguir acessar sites, você pode acessar o site que tem as UC's com seus arquivos dentro e fazer a organização para mim, nas uc's 1 e 2, os arquivos estão no site [https://ava.mg.senac.br/edu/course/view.php?id=18936](https://ava.mg.senac.br/edu/course/view.php?id=18936).

Nas atividades da uc3, alguns arquivos estão em repositorios publicado no git hub, la no site do ava tem os links para os repositorios.
