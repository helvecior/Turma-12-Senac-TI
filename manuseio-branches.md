# Comandos usados para a etapa inicial do repositório da turma

## Criação das branches em massa

### Versão que com o intuito de a branch 16 ser a mais antiga

``` bash
for i in {16..01}; do git checkout -b "UC$i"; git push -u origin "UC$i"; done
```

### Versão que com o intuito de a branch 16 ser a mais nova

``` bash
for i in {01..16}; do git checkout -b "UC$i"; git push -u origin "UC$i"; done
```

> **Nota:** Apesar de ambos comandos criarem as branches corretamente, nenhum dos dois comandos conseguiu fazer com que as branches ficassem na ordem do menor para o maior na lista de seleção de branches do GitHub.

## Apagando todas as branches locais e remotas

**Ambas versões visam apagar as branches locais e remotas, isso por conta de erros que estavam ocorrendo no processo de criação.**

### Comando usado para apagar todas as branches locais e remotas caso dê algum erro

``` bash
for i in {01..16}; do
  git push origin --delete "UC$i" ||  git push origin --delete "UC0$i";
  git branch -d "UC$i" || git branch -d "UC$i"; done
```

> **Nota:** Apesar de ter duas linhas separadas visualmente, o símbolo ; une as duas linhas. O símbolo || é usado para caso a primeira linha dê erro, ele executa a segunda linha, garantido que todas as branches sejam apagadas.

### Comando usado para apagar todas as branches locais e remotas, mantando a branch main como a branch ativa

``` bash
{
git checkout main
for i in {01..16}; do
  git push origin --delete "UC$i" ||  git push origin --delete "UC0$i";
  git branch -d "UC$i" || git branch -d "UC$i"; done
git checkout main
git branch
}
```

> **Nota:** Esse comando é uma variação do comando anterior, mas com a diferença de que ele muda para a branch main antes de apagar as branches, evitando o erro de não poder apagar a branch ativa.
